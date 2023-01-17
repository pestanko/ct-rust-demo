# CT Rust Demo

[Rust](https://www.rust-lang.org/) Demo for the Learning session

## Getting Started

Install the Rust using the [Rustup](https://rustup.rs/):

```shell
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

### Working with the Rustup

Update the rust version(s):

```shell
rustup update
```

For more information (for example install the `nightly` version of rust),
take a look [here](https://rust-lang.github.io/rustup/concepts/channels.html).

### Cargo (package manager)

Cargo is the Rust package manager. Cargo downloads your Rust package's dependencies, compiles your packages, makes distributable packages, and uploads them to crates.io, the Rust community’s package registry. You can contribute to this book on GitHub.

#### Create a new package

[Official documentation](https://doc.rust-lang.org/cargo/guide/creating-a-new-project.html)

```shell
# --bin is default (you will be creating an executable binary)
cargo new --bin my-ultimate-app
# --lib is for libraries
cargo new --lib my-ultimate-lib
```

Run the tests:

```shell
cargo test
```

Run the `main.rs` (for binary only):

```shell
cargo run
```

Add a dependency to your project - there are 2 options, you can either manually edit: `Cargo.toml` or run `cargo add`

Edit the `Cargo.toml` file:

```toml
[dependencies]
serde = { version = "1.0.152", features = ["derive"] }
```

Run the `cargo add`:

```shell
cargo add serde
# or with features
cargo add serde --features derive
```

### Rust-Analyzer (LSP)

Install the [`rust-analyzer`](https://rust-analyzer.github.io/):

- Extension for the [VSCode](https://marketplace.visualstudio.com/items?itemName=rust-lang.rust-analyzer)
- Manual installation [instructions](https://marketplace.visualstudio.com/items?itemName=rust-lang.rust-analyzer)

### Clippy (linter)

To use [Clippy](https://github.com/rust-lang/rust-clippy), you need to install it using the Rustup:

```shell
rustup component add clippy
```

Then you can run it:

```shell
cargo clippy
# or with fix
cargo clippy --fix
```

### Other tools

For other tools and components take a look:

- [Rustup Components](https://rust-lang.github.io/rustup/concepts/components.html) (example: `rustfmt`)

## Online learning resources

- [Rust Book](https://doc.rust-lang.org/book/)
- []
