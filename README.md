# sysma (System Maintenance)

**sysma** is a minimalist, one-click maintenance orchestrator for Debian and Ubuntu systems. It simplifies routine updates and cleanup tasks for standalone nodes and virtualization hosts (Proxmox/Incus).

## Features
- **Smart Updates:** Runs `apt update`, `apt dist-upgrade`, and `apt autoremove` in one go.
- **Virtualization Aware:** - Detects **Incus** and refreshes images/cleanups.
  - Handles **Proxmox** specific maintenance tasks.
- **Automated Cleanup:** Clears package caches and old kernels to save disk space.
- **Optional Reboot:** Flag to trigger a reboot only when necessary.

## Installation
To make `sysma` available system-wide:
```bash
sudo cp sysma /usr/local/bin/sysma
sudo chmod +x /usr/local/bin/sysma
