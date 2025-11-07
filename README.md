[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/rfay/ddev-acme-custom-commands/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/rfay/ddev-acme-custom-commands/actions/workflows/tests.yml?query=branch%3Amain)
[![last commit](https://img.shields.io/github/last-commit/rfay/ddev-acme-custom-commands)](https://github.com/rfay/ddev-acme-custom-commands/commits)
[![release](https://img.shields.io/github/v/release/rfay/ddev-acme-custom-commands)](https://github.com/rfay/ddev-acme-custom-commands/releases/latest)

# DDEV Acme Custom Commands

## Overview

This add-on integrates Acme Custom Commands into your [DDEV](https://ddev.com/) project.

## Installation

```bash
ddev add-on get rfay/ddev-acme-custom-commands
ddev restart
```

After installation, make sure to commit the `.ddev` directory to version control.

## Usage

| Command | Description |
| ------- | ----------- |
| `ddev describe` | View service status and used ports for Acme Custom Commands |
| `ddev logs -s acme-custom-commands` | Check Acme Custom Commands logs |

## Advanced Customization

To change the Docker image:

```bash
ddev dotenv set .ddev/.env.acme-custom-commands --acme-custom-commands-docker-image="ddev/ddev-utilities:latest"
ddev add-on get rfay/ddev-acme-custom-commands
ddev restart
```

Make sure to commit the `.ddev/.env.acme-custom-commands` file to version control.

All customization options (use with caution):

| Variable | Flag | Default |
| -------- | ---- | ------- |
| `ACME_CUSTOM_COMMANDS_DOCKER_IMAGE` | `--acme-custom-commands-docker-image` | `ddev/ddev-utilities:latest` |

## Credits

**Contributed and maintained by [@rfay](https://github.com/rfay)**
