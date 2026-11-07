# yapdf

A minimal, keyboard-driven PDF viewer in Rust, with vim bindings. The whole window is the document,
with a status line at the bottom. It has hint mode for selecting text from the keyboard, smart jump
and overview for following references, portals, search, annotations, fill & sign, and a themable
config that reloads while it runs.

A Linux x86-64 build is on the [releases page](https://github.com/araaha/yapdf/releases). To
build it yourself:

    cargo build --release -p yapdf
    target/release/yapdf file.pdf

Pushing a tag such as `v0.2.0` publishes a release, once `version` in `apps/yapdf/Cargo.toml`
says the same.

Keys, features and configuration are in [apps/yapdf/README.md](apps/yapdf/README.md), and
every setting with its default is in
[default_config.toml](apps/yapdf/src/default_config.toml).

## Where this comes from

yapdf is based on [PdfCraft](https://github.com/storytold/pdfcraft) by the ArtCraft team, and
uses its render engine and annotation writer. It is an independent project, not made, sponsored or
endorsed by them. The app is in `apps/yapdf`. The rest of this repository is PdfCraft, kept so
that the engine can follow upstream, with the ArtCraft logos removed from the current version as
their brand licence requires. Earlier commits are upstream's history, unchanged.

## Licence

MIT OR Apache-2.0, at your option: see [LICENSE-MIT](LICENSE-MIT), [LICENSE-APACHE](LICENSE-APACHE)
and [NOTICE](NOTICE). Bundled assets keep their own licences, listed in
[ATTRIBUTION.md](ATTRIBUTION.md).
