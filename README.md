# OrangeFox Recovery Project R12.0_1 (Unofficial)
### For Xiaomi Redmi 8 / 8A / 8A Dual / 7A (mi439 / olive / olivelite / olives / pine / olivewood)

- **Maintainer**: atsauban (Abdullah Atsa)
- **Branch**: fox_12.1-R (Android 12.1 manifest base)
- **Build Type**: Unofficial
- **Date**: 2026-10-07

---

### Features & Changelog:
- Initial Android 12.1 (`fox_12.1`) bringup for unified `mi439` Qualcomm SDM439 platform.
- Full support for `olive` (Redmi 8), `olivelite` (Redmi 8A), `olives` (Redmi 8A Dual/Pro), and `pine` (Redmi 7A).
- Dynamic partition & retrofit auto-detection support.
- Fully working multi-panel touchscreen support (FocalTech & Novatek).
- Flashlight / Torch toggle working with sysfs auto-detection.
- Persistent OrangeFox settings, Dark Theme, and gesture navigation.
- Backup, restore with MD5 digest verification tested and verified.
- Recovery PIN/Password protection support.
- MTP and ADB sideload support.

---

### Downloads:
- **Zip Installer**: `OrangeFox-R12.0_1_A12-Unofficial-mi439.zip` (Flash in current recovery)
- **Fastboot Image**: `recovery.img` (Flash via `fastboot flash recovery recovery.img`)

---

### Sources & Logs:
- **GitLab Device Tree**: https://gitlab.com/atsauban/recovery_device_xiaomi_mi439
- **Test Suite Logs**: https://gitlab.com/atsauban/recovery_device_xiaomi_mi439/-/tree/logs
