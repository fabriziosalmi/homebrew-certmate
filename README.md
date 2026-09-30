# homebrew-certmate

Homebrew tap for [**certmate-cli**](https://github.com/fabriziosalmi/certmate/tree/main/clients/certmate-cli), the command-line client for [CertMate](https://github.com/fabriziosalmi/certmate), the self-hosted TLS certificate lifecycle manager.

## Install

```bash
brew install fabriziosalmi/certmate/certmate-cli
```

Or tap first, then install:

```bash
brew tap fabriziosalmi/certmate
brew install certmate-cli
certmate --version
```

Point it at your instance:

```bash
export CERTMATE_URL=https://certmate.example.com
export CERTMATE_TOKEN=...   # an API key; prefer this over --token
certmate health
```

## What you get

The formula installs the `certmate` CLI from its PyPI release into its own virtualenv, with Homebrew's Python and every dependency pinned by sha256. Only the client: the CertMate server runs in Docker, Kubernetes or on a Linux host; see the [installation guide](https://github.com/fabriziosalmi/certmate/blob/main/docs/installation.md).

## Maintenance

The formula is kept in sync with the client releases by the certmate repository, where its source lives at [`deploy/homebrew/certmate-cli.rb`](https://github.com/fabriziosalmi/certmate/blob/main/deploy/homebrew/certmate-cli.rb). This repo is just the tap: issues and source live at [fabriziosalmi/certmate](https://github.com/fabriziosalmi/certmate).
