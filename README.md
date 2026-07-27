# xberg-io.r-universe.dev

R-universe package registry for the [Xberg](https://github.com/xberg-io) organization.

## Packages

| Package | Source Repository | Description |
|---------|-------------------|-------------|
| [xberg](https://xberg-io.r-universe.dev/xberg) | [xberg-io/xberg](https://github.com/xberg-io/xberg) | Extract text and metadata from 98+ file formats |
| [htmltomarkdown](https://xberg-io.r-universe.dev/htmltomarkdown) | [xberg-io/html-to-markdown](https://github.com/xberg-io/html-to-markdown) | High-performance HTML to Markdown converter |

## Installation

```r
# Install xberg
install.packages("xberg", repos = "https://xberg-io.r-universe.dev")

# Install htmltomarkdown
install.packages("htmltomarkdown", repos = "https://xberg-io.r-universe.dev")
```

## Status

- **htmltomarkdown** — builds and publishes on r-universe. ✅
- **xberg** — registered but **not yet building**: the R package pulls the full
  core feature set (ONNX/Paddle/candle/transcription), which won't compile on
  r-universe runners, and it isn't vendored for the isolated tarball build.
  Tracking + required fixes (align with `wasm-target`, regenerate the binding,
  vendor the Rust deps) are documented in
  [`xberg/packages/r/R-UNIVERSE.md`](https://github.com/xberg-io/xberg/blob/main/packages/r/R-UNIVERSE.md).

## Maintenance notes

- **This repo MUST be named `xberg-io.r-universe.dev`** (i.e.
  `xberg-io/xberg-io.r-universe.dev`), matching r-universe's `<owner>.r-universe.dev`
  convention. It was previously named just `r-universe.dev`, so r-universe never
  recognized it as the registry (the build repo
  [`r-universe/xberg-io`](https://github.com/r-universe/xberg-io) had no package
  submodules and `xberg-io.r-universe.dev` 404'd). Renaming fixed discovery.
- `packages.json` lists each package's source `url`, `branch` (`main`), and
  `subdir` (`packages/r`). r-universe rebuilds automatically on push here or to
  the source repos.

## Links

- [xberg-io.r-universe.dev](https://xberg-io.r-universe.dev)
- [Build status: r-universe/xberg-io](https://github.com/r-universe/xberg-io)
- [Xberg Documentation](https://xberg.io)
- [html-to-markdown Documentation](https://github.com/xberg-io/html-to-markdown)
