- [Compiling from Rust to WebAssembly - WebAssembly | MDN](https://developer.mozilla.org/en-US/docs/WebAssembly/Rust_to_wasm)

## Just a WWW

```console
$ wasm-pack build --target web
$ cd www
$ npm start
```

## Via a bundler

1. Build
2. Link the built npm package
3. Set up the app using the linked package

```console
$ wasm-pack build --target bundler
$ cd pkg
$ npm link
$ cd ../webpack
$ npm ci
$ npm link hello-wasm
$ npm start
```

Note that the `pkg/package.json` has a name `"hello-wasm"` there.
