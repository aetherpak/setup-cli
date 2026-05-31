# AetherPak Setup CLI GitHub Action

A GitHub Action to download and set up the AetherPak CLI (`aetherpak`) and install system-level dependencies.

> [!IMPORTANT]
> This action supports **Linux** (Ubuntu) runners only, for both **x86_64 / amd64** and **arm64** CPU architectures.

## Usage

Add the following step to your GitHub Actions workflow:

```yaml
- name: Set up AetherPak CLI
  uses: aetherpak/setup-cli@v1
  with:
    version: 'latest' # Or a specific version like 'v0.2.0'
```

## Inputs

| Input | Description | Default | Required |
| --- | --- | --- | --- |
| `version` | Version of AetherPak CLI to install (e.g., `v0.2.0`, `latest`) | `latest` | No |
| `repo` | GitHub repository containing the AetherPak CLI releases | `aetherpak/cli` | No |
| `install-dependencies` | Whether to automatically install missing system dependencies (`flatpak`, `ostree`, `flatpak-builder`) via `apt-get` on Linux | `true` | No |
