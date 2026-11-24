cd ~/orangefox/device/motorola/fogona

# 1. Create a clean README.md for your GitHub repo
cat << 'EOF' > README.md
# OrangeFox Recovery Device Tree for Motorola Moto G Play 2024 (`fogona`)

Unofficial OrangeFox (`fox_12.1`) device tree for **Motorola Moto G Play 2024** (`fogona` / Snapdragon 680 `bengal`), based on Android 14 stock firmware (`U1TFS34.100-35-14-1-18`).

## Device Specifications

| Feature | Specification |
| :--- | :--- |
| **SoC** | Qualcomm Snapdragon 680 (`SM6225` / `bengal`) |
| **Display** | 6.5" IPS LCD, 720x1600 (20:9), `tm_icnl9916c` |
| **Touchscreen** | Chipone TDDI (`chipone_tddi_v2_mmi`) |
| **Boot / Ramdisk** | Header v4, LZ4-compressed `vendor_boot` / `recovery` |

## Build Instructions
```bash
export ALLOW_MISSING_DEPENDENCIES=true
export FOX_BUILD_DEVICE="fogona"
source build/envsetup.sh
lunch twrp_fogona-eng
mka -j\$(nproc) recoveryimage
```
EOF

# 2. Initialize Git, commit all files, and push to GitHub
git init -b main
git config user.name "ddddddddddddds"
git config user.email "masterbitcionfoxy@gmail.com"
git add .
git commit -m "fogona: Initial OrangeFox R12.1 device tree (Android 14)"
git remote add origin https://github.com
git push -u origin main

### 🔗 Sources & Credits
* **OrangeFox Recovery Source (`fox_12.1`):** https://gitlab.com/OrangeFox
* **Device Tree (`device/motorola/fogona`):** https://github.com

