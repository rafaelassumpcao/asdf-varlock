# asdf-varlock

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

[asdf](https://asdf-vm.com) plugin for [varlock](https://github.com/dmno-dev/varlock).

## Install

```
asdf plugin add varlock https://github.com/rafaelassumpcao/asdf-varlock.git
asdf install varlock latest
asdf global varlock latest
```

## Supported platforms

Pulls prebuilt binaries from varlock's GitHub releases:

- macOS: arm64, x64
- Linux: x64, arm64 (glibc and musl)

Windows is not supported by this plugin (varlock ships a `.zip` there; asdf
itself targets Unix shells).

## Notes

- Release tags upstream are `varlock@X.Y.Z` (the monorepo also cuts releases
  for sibling packages under different tag prefixes), so `bin/list-all` filters
  strictly on that prefix.
- `bin/download` verifies the downloaded archive against upstream's
  `checksums.txt` before extracting.
