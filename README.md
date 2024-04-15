# qwe-rs

Rexports many `no_std` compile time mutually compatible boilerplate macros, primitives, traits and safe functions (written in unsafe Rust).

- derive-new
- displaydoc
- tuples
- num-traits
- derive_more
- bounded-collections
- enumn
- log
- strum
- ref-cast
- readonly
- inherent
- educe
- byteorder
- frunk
- result-like
- either

Provides several `Cargo.lock` and lockless branches, and ability to disable/enable crates behind feautes.. 

## Supply chain attack mitigation

- Builds them using `nix` sandbox ensuring `build.rs` and `macros` do not modify source code (read-only `src`) nor read/write from other folders.
- checks all deps via A and B advisor

## Nightly support

With `nightly` feature support works on latest  nightly supported by `nix`.

## Consistency

- renames some macros for consistency. For example `enum::N` renamed to `EnumNum`, like `num` crate.
