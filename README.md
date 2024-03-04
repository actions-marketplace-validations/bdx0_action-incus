# action-incus

action-incus setup [Incus](https://linuxcontainers.org/incus/) Server in GitHub Actions

## Usage

```
name: build

on:
  push:
  pull_request:

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - uses: bdx0/action-incus@v1

      - name: Launch instance
        run: |
          lxc launch images:ubuntu/focal build-server
```

## Inputs
