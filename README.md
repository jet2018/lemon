# Lemon 🍋

Lemon is an experimental, explicitly typed, object-oriented programming language intended to compile ahead of time to native machine code. Its frontend and initial reference interpreter will be written in Rust.

> Status: project scaffold only. No language syntax or runtime is implemented yet.

## Source files

Lemon recognizes `.lemon`, `.l`, and `.🍋` as equivalent source-file extensions. `.lemon` is the recommended conventional extension.

## Workspace

- `lemon-lexer`: tokenization
- `lemon-parser`: parsing
- `lemon-ast`: syntax tree data structures
- `lemon-semantics`: name resolution, types, ownership and borrowing
- `lemon-ir`: checked intermediate representation
- `lemon-interpreter`: reference execution engine
- `lemon-cli`: eventual `lemon` executable

## Getting started

Install Rust 1.85+ and run:

```sh
cargo check --workspace
cargo test --workspace
cargo run -p lemon-cli -- --help
```

The CLI currently prints a placeholder message. `lemon run` and native compilation are not yet implemented.

## Design process

Read `docs/specification/README.md` and `docs/decisions/0001-project-foundation.md`. Grammar and semantic choices will be written down and reviewed before implementation.

## License

MIT.
