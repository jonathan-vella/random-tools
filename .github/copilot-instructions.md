# jonnies-swiss-knife - AI Agent Instructions

## Project Guidelines

### Code Style
- **Python**: Use standard PEP 8 naming conventions. Prefer `pathlib` for file operations.
- **PowerShell**: Use PascalCase for function names and strictly use official `Az` module commands.
- **Markdown**: Use consistent heading levels and list structures for documentation.

### Architecture
- **Environment**: Container-first development repo using VS Code Dev Containers.
- **Base Image**: `mcr.microsoft.com/devcontainers/python:3.12-bookworm`.
- **Pre-installed Tools**:
  - **Azure CLI**: Version `latest` via devcontainer feature.
  - **Azure PowerShell**: With the official `Az` module pre-installed.
  - **Python 3.12+**: Core scripting environment.
  - **Pandoc**: Universal document converter.
- **Post-Create Setup**: Install `graphviz` (via apt) and `diagrams` (via pip) automatically.

### Build and Test
To verify the environment is ready for specific tasks, run these commands:
- **Azure CLI**: `az login` or `az --version`.
- **Azure PowerShell**: `pwsh -c "import-module Az; Get-Module Az"`.
- **Python Diagrams**: `python3 -c "import diagrams; print('Diagrams ready')"` and `dot -V`.
- **Pandoc**: `pandoc --version`.

### Project Conventions
- **Strict Git Tracking**: By design, this repo only tracks foundational configuration files.
  - Tracked: `README.md`, `.gitignore`, `.devcontainer/`, `.github/copilot-instructions.md`.
  - Untracked: All other folders (e.g., `diagrams/`, `scripts/`) are ignored to keep the repository clean.
- **File Organization**: Use descriptive subfolders like `diagrams/` for Python code, `azure/` for Az scripts, and `conversions/` for Pandoc tasks.
- **Reproducibility**: Ensure all required dependencies are added to `.devcontainer/devcontainer.json`.

### Major Components
1. **Python Diagrams**: Primary tool for architectural diagrams as code. Uses Graphviz.
2. **Azure Integration**: Dual-support for CLI and PowerShell (ARM64/x64 compatible).
3. **Document Conversion**: Pandoc for converting Markdown to various formats.
4. **General Scripting**: Python 3.12 for automation.
