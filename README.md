ansible-galaxy-import-action
============================

[![Tests](https://github.com/gantsign/ansible-galaxy-import-action/actions/workflows/tests.yml/badge.svg)](https://github.com/gantsign/ansible-galaxy-import-action/actions/workflows/tests.yml)

Imports a the current repo into Ansible Galaxy as a role.

Usage
-----

```yaml
name: Release

on:
  release:
    types:
      - published

jobs:
  release:
    name: Release
    runs-on: ubuntu-20.04
    steps:
      - name: Checkout
        uses: actions/checkout@v3

      - name: Import role into Ansible Galaxy
        uses: gantsign/ansible-galaxy-import-action@v1
        with:
          api-key: ${{ secrets.GALAXY_API_KEY }}
```

License
-------

The Unlicense

Author Information
------------------

John Freeman

GantSign Ltd.
Company No. 06109112 (registered in England)
