# Docker Compose Context Menu

Adds a cascading submenu to Windows File Explorer for running Docker Compose commands.

## Features
- True submenu with arrow in context menu
- Commands:
  - Docker Compose Up -d
  - Docker Compose Down
- Opens PowerShell 7 visibly in the folder you right-clicked

## Installation
1. Download `docker_compose_submenu.reg`.
2. Double-click to import into the registry.
3. Right-click inside any folder to see the **Docker Compose ▶** submenu.

## Requirements
- Windows 11
- PowerShell 7 installed and in PATH
- Docker installed and accessible via command line
