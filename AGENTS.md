# AGENTS.md

## Cursor Cloud specific instructions

### Repository Overview

This is a **Godot 4.6 GDScript game project** (based on the deleted `.cursorrules` conventions file in git history). As of the initial setup, the repository contains no source code, no project files, and no dependencies.

### Development Environment

- **Engine**: Godot 4.6 (GDScript) — requires a GUI display server to run the editor; headless export builds may be possible with Godot's CLI.
- **No package managers or dependency files** are present (no `package.json`, `requirements.txt`, `Cargo.toml`, etc.).
- **No build system** is configured (no Makefile, CMake, SCons, etc.).
- **No Docker services** are used.
- **No linting or testing frameworks** are configured yet.

### Notes for Future Agents

- Once Godot project files (e.g., `project.godot`) and GDScript source are added, the development environment will need the Godot Engine installed.
- Godot's editor requires a display server (X11/Wayland). In headless cloud VMs, use `--headless` flag for CLI operations (export, running tests via GUT framework, etc.).
- Refer to the git history (`git show a19c972:.cursorrules`) for the project's GDScript coding conventions.
