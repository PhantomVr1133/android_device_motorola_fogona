# OrangeFox Recovery R12.1 (Unofficial) — Motorola Moto G Play 2024 (`fogona`)

![Device](https://shields.io)
![Platform](https://shields.io)
![Recovery](https://shields.io)
![Maintainer](https://shields.io)

Unofficial **OrangeFox Recovery R12.1** device tree and prebuilt recovery image for the **Motorola Moto G Play 2024 (`fogona` / `XT2413`)**.

---

## 📱 Device Specifications

| Feature | Specification |
| :--- | :--- |
| **Device Name** | Motorola Moto G Play 2024 (`fogona`) |
| **Chipset** | Qualcomm Snapdragon 680 4G (`SM6225` / `bengal`) |
| **Display** | 6.5" IPS LCD, 720 × 1600 px (`2400` scaled UI), 90Hz |
| **Partition Scheme** | Virtual A/B with Dynamic `super` Partitions |
| **Supported Firmware** | Stock Android 14 (`U1TFS34.100-35-14-1-18`) |
| **Maintainer** | `(XDA : ddddddddddddds)` ([PhantomVr1133](https://github.com)) |

---

## ✨ Key Features
* **Bootloader-Compliant 32 MB Ramdisk:** Compressed LZ4 ramdisk is **~28.56 MB (`29,950,834` bytes)** with a 4,096-byte AVB hash footer, staying safely below Motorola's strict 32 MB (`33,554,432`-byte) recovery partition limit.
* **Full Touchscreen & Haptic Support:** Supports Chipone, Novatek, and Ilitek touchscreen panels alongside Motorola's `ldo_vibrator_mmi` haptic motor.
* **A/B `slotselect` Backup & Restore:** Properly configured `recovery.fstab` for `boot`, `init_boot`, `dtbo`, `vendor_boot`, `super`, and `data`.
* **Working USB ADB & MTP:** Dynamic Type-C peripheral gadget configuration for seamless file transfers and sideloading.
* **Two-Tier Developer & Admin Tools:**
  * **Developer Options (User):** Unlocked via **7 taps** on **Version** inside **Menu → Settings → About**. Includes battery/thermal diagnostics, touchscreen panel detection, USB rebind, and A/B slot switching.
  * **6-Step Admin Vault & 30-Tool Admin Panel:** Protected by a **6-step Vault sequence** with **3-strike automatic reboot** protection, unlocking **30 maintainer tools** (raw partition backups, `lpdump`/`dmsetup` inspection, dynamic `/vendor` & `/system_root` mounting, FBE/Keymint status, `adbd` restart, and full `getprop`/`dmesg` exports).

---

## ⚠️ Important Notes
* **Stock Android 14 Firmware Only:** Built with Stock Android 14 (`U1TFS34.100`) kernel modules. Do **not** flash this `recovery.img` over Android 17 custom ROMs (such as LineageOS 24.0), as mismatched kernel modules will cause a recovery bootloop.
* **Backing Up `Super`:** Always select **MicroSD** or **USB OTG** as the destination when backing up the ~9 GB `Super` partition image.

---

## 📲 Installation
1. Boot your device into **Fastboot / Bootloader** mode (**Power + Volume Down**).
2. Flash the recovery image:
   ```bash
   fastboot flash recovery recovery.img
   ```
3. Highlight **Recovery mode** using **Volume Down** and press **Power** to boot into OrangeFox Recovery.
4. *(Optional)* Flash `OrangeFox-R12.0_0-Unofficial-fogona.zip` via **Menu → ADB Sideload** to install `/sdcard/Fox/` files.

---

## 📜 Credits & License
* **OrangeFox Recovery Team** for the base recovery source and UI.
* **Maintainer:** `(XDA : ddddddddddddds)`
* Licensed under the **GNU General Public License v3.0 (GPL-3.0)**.

