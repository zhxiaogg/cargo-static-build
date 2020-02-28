# Cargo Static Build Docker Action

This action builds sttic linked binaries for rust projects, using [clux/muslrust](https://github.com/clux/muslrust).

## Inputs

### cmd

Buld command, default to `cargo build`.

## Outputs

None.

## Example usage

```yaml
name: Cargo Static Build

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
    - name: Build and Test
      uses: zhxiaoggg/cargo-static-build-action@master
      with:
        cmd: cargo test
```
