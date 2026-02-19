SYSMA SYSTEM MAINTENANCE

sysma is a minimalist one-click maintenance orchestrator for Debian and Ubuntu systems. It simplifies routine updates and cleanup tasks for standalone nodes and virtualization hosts Proxmox and Incus.

FEATURES

    Smart Updates: Runs apt update, apt dist-upgrade, and apt autoremove in one sequence.

    Virtualization Aware: Detects Incus to refresh images and perform cleanups and handles Proxmox specific maintenance routines.

    Automated Cleanup: Clears package caches and removes old kernels to reclaim disk space.

    Efficient Workflow: Designed to be run manually or via cron for consistent server health.

INSTALLATION
To make sysma available system-wide:
sudo cp sysma /usr/local/bin/sysma
sudo chmod +x /usr/local/bin/sysma

USAGE
Run the script with root privileges:
sudo sysma [options]

OPTIONS
Flag -r: Reboot the system automatically after maintenance is complete.
Flag -p: Proxmox and Incus Mode including specific container and hypervisor optimizations.

EXAMPLES

    Standard maintenance:
    sudo sysma

    Full Hypervisor Refresh:
    sudo sysma -p

    The Update and Reboot cycle:
    sudo sysma -p -r

Developed by njvdh (https://github.com/njvdh) as part of the infrastructure toolkit.
