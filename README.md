# Docker Compose Context Menu

Adds a **Docker Compose** submenu to the Windows File Explorer right-click
menu, so you can manage a Compose project without typing commands.

## Commands

| Menu item | Runs |
|---|---|
| Up -d | `docker compose up -d` |
| Pull & Up -d | `docker compose pull; docker compose up -d` (update images, then restart what changed) |
| Status (ps) | `docker compose ps` |
| Logs (follow) | `docker compose logs -f --tail 100` (press Ctrl+C to stop) |
| Down | `docker compose down` (stops and removes the containers; volumes and data are kept) |

Each command opens a PowerShell 7 window in that folder and stays open, so
you can read the output or any error.

The menu appears in two places:
- right-click the **empty space inside** a folder that holds a `compose.yaml`
  / `docker-compose.yml`;
- right-click **on** such a folder.

Folder names with spaces or apostrophes work.

## Installation
1. Download `docker_compose_context.reg`.
2. Double-click it and confirm. It installs for **your user account only**
   (`HKEY_CURRENT_USER`), so no administrator rights are needed.
3. **Windows 11:** classic menu entries like this one are under
   **Show more options** (or press **Shift+F10**) — Windows 11's compact
   menu doesn't show them.

**Upgrading from the original 2025 version?** That version was installed
machine-wide. Double-click `uninstall-old-version.reg` first (it needs
administrator rights), then install as above.

## Uninstall
Double-click `uninstall.reg`.

## Requirements
- Windows 10 or 11
- [PowerShell 7](https://github.com/PowerShell/PowerShell) (`pwsh.exe`) installed
- Docker Desktop (or another Docker engine with the `docker compose` plugin)
  installed and working from the command line

The icons come from the default install locations of Docker Desktop
(`C:\Program Files\Docker\Docker\Docker Desktop.exe`) and PowerShell 7
(`C:\Program Files\PowerShell\7\pwsh.exe`); if yours live elsewhere the
menu still works, only the icons are missing.
