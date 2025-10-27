# Setup Chisel Action

A GitHub Action to download, verify, and install [Canonical Chisel](https://github.com/canonical/chisel).

## Features
- Supports pinned versions
- Supports `latest` mode
- Verifies SHA-384 checksums
- Detects runner architecture (amd64, arm64, arm, ppc64le, riscv64, s390x)
- Adds `chisel` to PATH using `$GITHUB_PATH`

## Usage

### Pin to a specific version
```yaml
- uses: Mattheish/setup-chisel-action@v1
  with:
    version: v1.3.0
```