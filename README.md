# jonnies-swiss-knife

A multi-purpose, cross-platform dev tool repository for random tooling tasks.

## Purpose

This project is built to handle:
- **Diagrams as Code**: Using Python with the `diagrams` library (requires Graphviz).
- **Azure Automation**: Azure CLI and Azure PowerShell Core (fully ARM64 and x64 compatible).
- **Document Conversion**: Markdown to other formats via Pandoc.
- **Python Scripting**: General-purpose Python scripts.

## Core Tools Included

The devcontainer is optimized for x64 and ARM64 architecture (e.g., Apple Silicon, ARM Linux) and includes the following:

| Tool | Purpose |
| :--- | :--- |
| **Azure CLI** | Infrastructure and cloud management via CLI. |
| **Azure PowerShell** | Automation with the official `Az` module. |
| **Python 3.12** | Core programming language for scripts. |
| **Diagrams (Python)** | Creating system/architecture diagrams from code. |
| **Graphviz** | Engine behind diagram rendering. |
| **Pandoc** | Universal document converter for Markdown. |

## Quick Start

1. Open this repository in **VS Code**.
2. When prompted, click **Reopen in Container**.
3. All dependencies will be automatically installed.

## Project Structure Guidance

Only the following are tracked in Git:
- `README.md`
- `.devcontainer/`
- `.gitignore`

Feel free to create subdirectories for specific tools (e.g., `diagrams/`, `azure-scripts/`, `conversions/`), but note they will not be committed to Git unless you modify `.gitignore`.
