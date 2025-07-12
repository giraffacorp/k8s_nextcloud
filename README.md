# Kubernetes Application Template Repository

This repository serves as a template for deploying applications to Kubernetes clusters using ArgoCD's "App of Apps" pattern. It provides a structured, maintainable approach to managing Kubernetes applications with built-in support for secrets management via SOPS, automated dependency updates with Renovate, and streamlined workflows through Taskfile.

## Components Overview

- **nexcloud**: file sharing server

## Repository Structure

```
├── .taskfiles/                 # Custom Taskfile scripts modules
├── apps/                       # Core application configurations
├── argocd/                     # ArgoCD definitions
│   ├── app-of-apps.yaml
│   └── applications/
├── .envrc                      # Direnv environment variables
├── .gitattributes              # Git attributes configuration
├── .gitignore                  # Git ignore rules
├── .pre-commit-config.yaml     # Pre-commit hooks configuration
├── .sops.yaml                  # SOPS encryption configuration
├── gitleaks.toml               # Gitleaks secret scanning configuration
├── renovate.json               # Renovate dependency management
├── taskfile.yaml               # Task runner definitions
└── yamlfmt.yaml                # YAML formatting configuration
```

## Prerequisites

- [Task](https://taskfile.dev/) - Task runner tool
- [direnv](https://direnv.net/) - Environment variable management
- [SOPS](https://github.com/mozilla/sops) - Secret management
- [age](https://github.com/FiloSottile/age) - Encryption tool
- [uv](https://docs.astral.sh/uv/) - Python package management

