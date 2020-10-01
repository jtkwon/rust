# Hello Cargo
---
`Cargo` is Rust's build system and package manager.
It builds, downloads libraries, and build those dependencies.

**To check version**
```
$ cargo --version
```

### Creating a Project with Cargo
```
$ cargo new hello_cargo
```

This will create 
- src folder
- Cargo.toml (Tom's Obvious, Minimal Language) configuration format
- It also initialized a new Git repository along with a .gitignore file
**Git won't be generated if you run `cargo new` within an existing Git repository**

*Cargo.toml*
The first line `[package]` is a configuration section
`[dependencies]` is section to list any of your project's dependencies.

In rust, dependencies or packages of codes are called `crated`.

Cargo expects resource files to live inside the `src` directory.
The top-level project directory is just for README files, license information, configuration files, and anything that is not related to your code.


### Building and Running a Cargo Project
**Building**
```
$ cargo build
```
- Building the Cargo project will automatically create a `target` folder.
- It creates an executable file withint `./target/debug/<name>`
- Running `cargo build` for the first time will also create `Cargo.lock`.  It keep versions of dependencies (Similar to package.lock)

**Build and Run**
```
$ cargo run
```
- It builds and runs

**Checks code without creating executable**
```
$ cargo check
```
- Checking is much faster than compiling and running
- It helps to check to make sure program compiles

**Building for release**
```
$ cargo build --release
```
- Adding `--release` tag after the build command will compile it with optimization.
- Will create executable in `target/release`
- Optimization makes your code run faster but it takes longer to compile.
