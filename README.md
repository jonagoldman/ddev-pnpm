[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/jonagoldman/ddev-pnpm/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/jonagoldman/ddev-pnpm/actions/workflows/tests.yml?query=branch%3Amain)
[![last commit](https://img.shields.io/github/last-commit/jonagoldman/ddev-pnpm)](https://github.com/jonagoldman/ddev-pnpm/commits)
[![release](https://img.shields.io/github/v/release/jonagoldman/ddev-pnpm)](https://github.com/jonagoldman/ddev-pnpm/releases/latest)

# DDEV `pnpm`

## Overview

This add-on integrates `pnpm` into your [DDEV](https://ddev.com/) project.

## Installation

```bash
ddev add-on get jonagoldman/ddev-pnpm
ddev restart
```

After installation, make sure to commit the `.ddev` directory to version control.

## Usage

```sh
ddev pnpm
```

Please refer to the documentation at [pnpm.io](https://pnpm.io)

### Working directory

By default, this add-on assumes your `package.json` is in the root of the DDEV project.

In a monorepo, such as the one below, `package.json` is in `frontend`.

```md
.
├── .ddev
├── backend/
│   └── composer.json
└── frontend/
    └── package.json
```

To configure this addon to run PNPM commands for this example project, set a `PNPM_DIRECTORY` environment variable to `frontend`. For example: `.ddev/.env`

```env
PNPM_DIRECTORY=frontend
```

## Credits

**Contributed and maintained by [@jonagoldman](https://github.com/jonagoldman)**
