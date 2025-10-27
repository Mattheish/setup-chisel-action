# Setup Chisel Action

A GitHub Action to download, verify, and install [Canonical Chisel](https://github.com/canonical/chisel) with optional support for the [`chisel-wrapper`](https://github.com/canonical/rocks-toolbox) helper script.

`chisel` is always added to `PATH`. `chisel-wrapper` is installed only when explicitly requested.

## Features
- Supports pinned versions (e.g. `v1.3.0`) or `latest`
- Verifies SHA-384 checksums for integrity
- Auto-detects runner architecture: `amd64`, `arm64`, `arm`, `ppc64le`, `riscv64`, `s390x`
- Installs `chisel` to `$PATH` by default
- Optionally installs `chisel-wrapper` (opt-in via `install-wrapper: true`)

## Usage

### Pin to a specific version
```yaml
- uses: Mattheish/setup-chisel-action@v1.1.0
  with:
    version: v1.3.0
    install-wrapper: true
```