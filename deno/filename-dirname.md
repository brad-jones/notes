# Deno Equivalent of `__filename` & `__dirname`

In Deno, there aren't variables like `__dirname` or `__filename` but you can get the same values thanks to `import.meta.url`.

```ts
import * as path from "https://deno.land/std/path/mod.ts";
const __filename = path.fromFileUrl(import.meta.url);
const __dirname = path.dirname(__filename);
```

<https://stackoverflow.com/questions/61829367>