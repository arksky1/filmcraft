# Korean translation validation

Catalog additions against `70f0fc7a75f2681bc18302e67eaf0c9d41c68873`: **4** entries. Existing Korean entries are unchanged. The provided translation data was checked against the current Rust sources; candidate keys with no matching production literal were excluded. No new translations were generated.

## Static checks

- Catalog structure, unique keys, original key preservation, named placeholders, trailing ellipses, and explicit shortcut tokens checked with Python 3.14.5.
- Existing catalog entries were compared with the baseline commit.
- New entries have source-location evidence in the local audit; dynamic labels use the existing translation paths.
- `git diff --check` passed.

## Checks not run

Cargo, rustc, and rustfmt are unavailable in this environment. Rust installation is awaiting user approval; no tools were installed. The following checks have **not** been run:

- `cargo test -p filmcraft-ui-egui`
- `cargo fmt --all --check`
- `cargo clippy -p filmcraft-ui-egui --all-targets -- -D warnings`
- `cargo xtask layers`, `cargo xtask assets`, `cargo xtask wasm`, and the full `cargo xtask ci` gate
- Native and web UI rendering, layout, runtime language switching, and font/glyph coverage

## Candidate filtering

- Excluded 0 supplied candidate keys without a matching production source literal.
- Excluded 0 supplied keys already proposed in open Korean translation PRs.

The Korean no-dead-entry test now accepts exact `t("…")` calls in the desktop audio warning source, because those messages have not yet been added to the Spanish catalog. The obsolete VA-API-only paragraph was not added. The Rust test was updated but not executed.
