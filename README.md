# wasmer-rust-embed-wasm
Example code to load a wasm file, add.wasm, into a RUST file and calling the function in the RUST file.

To run it: `$ cargo run `

You should see:
```
Compiling module...
Instantiating module...
Calling `add_one` function...
Results of `add_one`: 1234
```

Environmentt needed: 
(1) Install wasmer:
```
$ curl https://get.wasmer.io -sSfL | sh
$ wasmer config --pkg-config
prefix=/Users/USER/.wasmer
exec_prefix=/Users/USER/.wasmer/bin
includedir=/Users/USER/.wasmer/include
libdir=/Users/syrus/.wasmer/lib

Name: wasmer
Description: The Wasmer library for running WebAssembly
Version: 2.0.0
Cflags: -I/Users/USER/.wasmer/include/wasmer
Libs: -L/Users/syrus/.wasmer/lib -lwasmer
```

(2) Install RUST
```
$ curl https://sh.rustup.rs -sSf | sh
$cargo --version
```

Tools you may want:

https://github.com/WebAssembly/wabt - for example: wasm2wat add.wasm -o add.wat - this reverse binary to S expression, human readable text, for debugging purpose
https://docs.rs/wasmer/2.0.0/wasmer/ wasm API in RUST document
