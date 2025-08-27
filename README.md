# -Dual-Boot-to-Single-Boot-Migration-Dell-OptiPlex-7050
Move from a dual-boot setup (Linux Mint on SSD + Windows 11 on HDD) to a single Windows 11 install on the SSD, using the HDD only for storage.


🔹 Steps
1. Backup

Saved any important files from both Linux Mint and Windows HDD before wiping drives.

2. Create Windows 11 Installer

Downloaded Microsoft’s Media Creation Tool.

Created a bootable USB installer (8GB+).

3. Install Windows 11 on SSD

Booted from USB (F12 at Dell logo).

Chose Custom: Install Windows only (advanced).

Deleted all partitions on SSD.

Installed Windows 11 fresh to SSD.

4. BIOS Boot Order Fix

After reboot, system defaulted to GRUB (Ubuntu) from HDD.

Entered BIOS Setup (F2) → Boot Sequence.

Moved Windows Boot Manager (SSD) to the top.

Disabled/removed the old Ubuntu entry.

5. Dual Windows Boot Screen

On restart, system showed two Windows 11 options (“Volume 3” and “Volume 6”).

Tested each:

SSD Windows = boots normally.

HDD Windows = black screen / not bootable.

6. Remove Old Boot Entry

Booted into SSD Windows.

Ran msconfig → Boot tab.

Deleted the non-working Windows 11 entry.

7. Reformat HDD for Storage

Opened Disk Management (Win + X → Disk Management).

Deleted all partitions on HDD.

Created a New Simple Volume, formatted as NTFS, assigned drive letter (e.g., D:).

🔹 End Result

Windows 11 boots directly from SSD (fast and clean).

HDD is formatted and used only as storage.

GRUB and extra boot entries fully removed.
