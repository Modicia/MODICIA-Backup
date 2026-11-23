# MODICIA Backup

Designed for **MODICIA O.S.**, Debian-based GNU/Linux systems, and **Windows 11**, **MODICIA Backup** is a cross-platform tool engineered to do one thing right: safely backing up and restoring a folder from a disk to an external storage device (USB, SSD, HDD) or another folder, and vice versa, eliminating the risk of data corruption or filename incompatibility.

## Supported Platforms

- **MODICIA O.S.** & Debian-based GNU/Linux distributions (`.deb`, `.AppImage`)
- **Windows 11** (`.exe`, `.msi`)

## Key Features

- **Safe `.7z` Encapsulation**: Compresses (or encapsulates uncompressed by default using `-mx=0`) files while preserving unusual filenames, special characters (`?`, `:`, `<`, `>`, `|`, `"`), spaces, and symbolic links that would otherwise fail during cross-platform transfers across FAT32, exFAT, NTFS, or ext4 drives.
- **2-Step Process with Dual Progress Bars**:
  1. **Action 1/2 (Compression)**: Creates the `.7z` archive with selectable compression levels and optional **AES-256** password protection (including filename encryption).
  2. **Action 2/2 (Saving & Bit-by-Bit Verification)**: Transfers the archive to the final destination, forces hardware buffer flushing (`fsync` / `sync` on Linux, native OS write flush on Windows 11), and performs a full read-back from the disk.
- **Guaranteed Safe Removal**: The application reports the backup as complete only when the file is physically written to the external drive and verified bit-for-bit (**SHA-256**).

---

## Quick Start Guide

### 1. How to Perform a Safe Backup

1. Select the **Source Folder** to back up by clicking **BROWSE SOURCE** (or by dragging and dropp<img width="640" height="360" alt="backup" src="https://github.com/user-attachments/assets/e4de9a6c-1f10-4498-ae51-3472291fee60" />
ing it into the window).
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
<img width="1080" height="847" alt="Schermata del 2026-11-23 18-57-06" src="https://github.com/user-attachments/assets/93eaf027-d3bf-458b-8b8b-b376781739b8" />
<img width="1080" height="847" alt="Schermata del 2026-11-23 18-56-56" src="https://github.com/user-attachments/assets/e10f253b-aef8-4049-9095-5a649c36b71c" />
<img width="780" height="718" alt="Schermata del 2026-11-23 18-56-43" src="https://github.com/user-attachments/assets/428933cd-b33f-4190-aa5d-a6d4871b1261" />
<img width="780" height="718" alt="Schermata del 2026-11-23 18-56-26" src="https://github.com/user-attachments/assets/8ae14cc7-89c0-4f8d-bf93-962dc85b2811" />
<img width="780" height="718" alt="Schermata del 2026-11-23 18-56-11" src="https://github.com/user-attachments/assets/621e631f-947a-4cac-9cc0-3bd887a50dca" />
