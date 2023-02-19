# Code along Zero to Production

This repository contains a basic Rust application that serves a newsletter mailing list. The code is to learn from the book "Zero to Production" for the programming list Rust. 

## Tooling

### cargo-watch
 Monitors source code to trigger commands every time a file changes.

install:
```bash
cargo install cargo-watch
```

```bash
cargo watch -x check -x test -x run
```

### Code Coverage

The author is recommending 'cargo-tarpaulin'. 

install: 
```bash
cargo install cargo-tarpaulin
```

```bash
cargo tarpaulin --ignore-tests
```

### Linting

Code linting is done by clippy. 

```
rustup component add clippy
```

Use locally with

```
cargo clippy
```

In the CI pipeline the next command will let clippy fail if it finds something

```
cargo clippy -- -D warnings
```

### Formatting

The author recommends to use rustfmt to format the code.
```
rustup component add rustfmt
```

You can format your whole project with

```
cargo fmt 
```

In our CI pipeline we will add a formatting step

```
cargo fmt -- --check 
```

It will fail when a commit contains unformatted code, printing the difference to the console


### Security Scanner

The book recommends to use cargo-audit. 

```
cargo install cargo-audit
```

Use like this
```
cargo audit
````
