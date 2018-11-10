# reproduce ice: 

[issues-55723](https://github.com/rust-lang/rust/issues/55723)

Rust Version: `rustc 1.32.0-nightly (8b096314a 2018-11-02)`

```rust
$ cargo doc
```

Output:

```rust
Documenting test_ice v0.1.0 (/work/projects/rust/test_ice)
thread '<unnamed>' panicked at 'assertion failed: bpos.to_u32() >= mbc.pos.to_u32() + mbc.bytes as u32',libsyntax/source_map.rs:842:17
note: Run with `RUST_BACKTRACE=1` for a backtrace.

error: internal compiler error: unexpected panic

note: the compiler unexpectedly panicked. this is a bug.

note: we would appreciate a bug report: https://github.com/rust-lang/rust/blob/master/CONTRIBUTING.md#bug-reports

note: rustc 1.32.0-nightly (8b096314a 2018-11-02) running on x86_64-apple-darwin

error: Could not document `test_ice`.

Caused by:
  process didn't exit successfully: `rustdoc --edition=2018 --crate-name test_ice src/lib.rs --color always -o /work/projects/rust/test_ice/target/doc -L dependency=/work/projects/rust/test_ice/target/debug/deps` (exit code: 1)
```
