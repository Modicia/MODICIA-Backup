# MODICIA Backup

Designed for **MODICIA O.S.** and Debian-based GNU/Linux systems, **MODICIA Backup** is a dedicated tool engineered to do one thing right: safely backing up and restoring a folder from a disk to an external storage device (USB, SSD, HDD) or another folder, and vice versa, eliminating the risk of data corruption or filename incompatibility.

## Key Features

- **Safe `.7z` Encapsulation**: Compresses (or encapsulates uncompressed by default using `-mx=0`) files while preserving unusual filenames, special characters (`?`, `:`, `<`, `>`, `|`, `"`), spaces, and symbolic links that would otherwise fail during transfers to FAT32, exFAT, or NTFS drives.
- **2-Step Process with Dual Progress Bars**:
  1. **Action 1/2 (Compression)**: Creates the `.7z` archive with selectable compression levels and optional **AES-256** password protection (including filename encryption).
  2. **Action 2/2 (Saving & Bit-by-Bit Verification)**: Transfers the archive to the final destination, forces hardware buffer flushing (`fsync` / `sync`), and performs a full read-back from the disk.
- **Guaranteed Safe Removal**: The application reports the backup as complete only when the file is physically written to the external drive and verified bit-for-bit (**SHA-256**).

---

## Quick Start Guide

### 1. How to Perform a Safe Backup

1. Select the **Source Folder** to back up by clicking **BROWSE SOURCE** (or by dragging and dropping it into the window).
2. Select the **Final Destination** by clicking **BROWSE DESTINATION**, or pick your USB drive directly from the **External Media / Detected Drives** menu.
3. Use the **⇄ SWAP SOURCE / DESTINATION** button to switch the two folders on the fly.
4. Choose the **Compression Type**: set to **No Compression (`-mx=0`)** by default for maximum speed and reliability, with **Fast**, **Normal**, **Maximum**, and **Ultra** also available.
5. To protect your backup, check **Protect archive with Password** (**AES-256** encryption with encrypted filenames).
6. Click **START SAFE BACKUP (.7z)** and follow the two progress bars (**First: Compression**, **Second: Saving and Bit-by-Bit Verification**).

### 2. How to Perform a Restore

1. Switch to the **RESTORE ARCHIVE (.7z)** tab.
2. Select the `.7z` archive to restore and the destination folder.
3. If the archive is password-protected, enter the password in the dedicated field.
4. Click **START SAFE RESTORE**: the program will first verify the archive's integrity, extract all files, and physically sync the disk.

---

## Author, Website & License

- **Author**: Marco M. Mariani & MODICIA O.S. Development Team (`Marco M. Mariani for MODICIA O.S.`)
- **Website**: [https://www.modiciaos.cloud](https://www.modiciaos.cloud)
- **License**: GNU GPLv3 & Creative Commons Attribution 4.0 International (CC BY 4.0)
