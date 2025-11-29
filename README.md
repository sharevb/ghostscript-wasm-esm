# ghostscript-wasm-esm

This is a fork of [ghostscript-wasm](https://github.com/jsscheller/ghostscript-wasm/) that uses ESM instead of CommonJS and with TypeScript typing.

Since Ghostscript is huge wasm, it is NOT embedded in JS. You need to copy gs.wasm to a public directory of your app.

It is adjusted for the browser and has the following differences due to changes in build options:
- It is an ES module instead of a CommonJS module.
- It names the exported default function `gs` instead of `Module`(default name).
- It build `gs.mjs` instead of `gs.js`.
- It accepts overloading of the `print` and `printErr` methods.
- It provides TypeScript typing

# Examples

Build with docker (run `./docker_build.sh`) and run see the `tests/test.html`.

---

# ghostscript-wasm-esm

`ghostscript` compiled to WASM via Emscripten.

```sh
npm install --save ghostscript-wasm-esm
```

## Examples

See the `tests` directory for examples.
