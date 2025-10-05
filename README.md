[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/jonagoldman/ddev-pnpm/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/jonagoldman/ddev-pnpm/actions/workflows/tests.yml?query=branch%3Amain)
[![last commit](https://img.shields.io/github/last-commit/jonagoldman/ddev-pnpm)](https://github.com/jonagoldman/ddev-pnpm/commits)
[![release](https://img.shields.io/github/v/release/jonagoldman/ddev-pnpm)](https://github.com/jonagoldman/ddev-pnpm/releases/latest)

# DDEV Pnpm

## Overview

This add-on integrates Pnpm into your [DDEV](https://ddev.com/) project.

## Installation

```bash
ddev add-on get jonagoldman/ddev-pnpm
ddev restart
```

After installation, make sure to commit the `.ddev` directory to version control.

## Usage

| Command | Description |
| ------- | ----------- |
| `ddev describe` | View service status and used ports for Pnpm |
| `ddev logs -s pnpm` | Check Pnpm logs |

## Advanced Customization

To change the Docker image:

```bash
ddev dotenv set .ddev/.env.pnpm --pnpm-docker-image="ddev/ddev-utilities:latest"
ddev add-on get jonagoldman/ddev-pnpm
ddev restart
```

Make sure to commit the `.ddev/.env.pnpm` file to version control.

All customization options (use with caution):

| Variable | Flag | Default |
| -------- | ---- | ------- |
| `PNPM_DOCKER_IMAGE` | `--pnpm-docker-image` | `ddev/ddev-utilities:latest` |

## Credits

**Contributed and maintained by [@jonagoldman](https://github.com/jonagoldman)**
