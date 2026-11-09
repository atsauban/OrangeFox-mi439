# OrangeFox Recovery Project R12.0_3 (Unofficial)

Unofficial OrangeFox Recovery builds for Xiaomi Redmi 8 / 8A / 8A Dual / 7A / 8A Pro (`mi439`).

- **Maintainer**: atsauban
- **Version**: R12.0_3
- **Branch**: `fox_12.1-R`
- **Supported devices**: Xiaomi Redmi 8 (`olive`), Redmi 8A (`olivelite`), Redmi 8A Dual (`olives`), Redmi 7A (`pine`), Redmi 8A Pro (`olivewood`)

---

## Which build should I download?

Due to differences in encryption architecture and kernel versions, OrangeFox is provided in **two variants**:

### 1. FBEv1 Variant (Kernel 4.9)
Use this if you are running:
- Official Stock MIUI (MIUI 10, 11, or 12)
- Older Custom ROMs running Android 9, 10, 11, or 12 (Kernel 4.9)
- Non-dynamic Android 13 ROMs

### 2. FBEv2 Variant (Kernel 4.19)
Use this if you are running:
- Modern Custom ROMs running Android 13, 14, 15, 16, or 17 (Kernel 4.19+)
- Retrofit Dynamic Partition ROMs (such as LineageOS)

If you are unsure, most stock MIUI and older custom ROM users need FBEv1.

---

## Downloads


| Variant | Target ROMs | Recovery ZIP | Fastboot IMG | MD5 |
|---|---|---|---|---|
| **FBEv1** | Stock MIUI / Android 9–12 (Kernel 4.9) | [Download ZIP](https://github.com/atsauban/OrangeFox-mi439/releases/download/R12.0_3_A12-Unofficial/OrangeFox-R12.0_3_FBEv1-Unofficial-mi439.zip) | [Download IMG](https://github.com/atsauban/OrangeFox-mi439/releases/download/R12.0_3_A12-Unofficial/OrangeFox-R12.0_3_FBEv1-Unofficial-mi439.img) | `405a2cb531ce958185374eaf500eec3b` |
| **FBEv2** | Android 13–17 / Dynamic (Kernel 4.19) | [Download ZIP](https://github.com/atsauban/OrangeFox-mi439/releases/download/R12.0_3_A12-Unofficial/OrangeFox-R12.0_3_FBEv2-Unofficial-mi439.zip) | [Download IMG](https://github.com/atsauban/OrangeFox-mi439/releases/download/R12.0_3_A12-Unofficial/OrangeFox-R12.0_3_FBEv2-Unofficial-mi439.img) | `7c114ef41b07e95fa726d1ecd34cf42c` |

---

## How to Install

### Option A: From Existing Custom Recovery
1. Download the `.zip` file for your variant.
2. Transfer it to your phone storage or MicroSD card.
3. Reboot to recovery, select the `.zip` file, and swipe to flash.
4. OrangeFox will reboot the recovery automatically.

### Option B: From Fastboot via PC
1. Download the `.img` file for your variant.
2. Boot phone into Fastboot mode (hold **Volume Down + Power**).
3. Connect the phone to your PC and flash via terminal:
   ```bash
   fastboot flash recovery <image_name>.img
   fastboot reboot recovery
   ```
4. Hold **Volume Up** while rebooting until the OrangeFox splash screen appears.

---

## Changelog (R12.0_3)

- **FBEv1 Lockscreen Decryption Fix**: Resolved synthetic password decryption failure on Android 11 custom ROMs when a PIN/password is set by bridging legacy keystore files to Keystore 2.0.
- **FBEv2 Modern Encryption**: Support FBE Policy v2 (`fscrypt` v2 + `inlinecrypt_optimized` + `metadata_encryption=aes-256-xts`) for Android 13–17 ROMs on Linux 4.19.
- **MicroSD Card Mounting**: Support auto filesystem detection (exFAT, FAT32, ext4) and fallback block device (`mmcblk1`).
- **Storage**: dual filesystem support (`f2fs` & `ext4`) on userdata.

---

## Links & Sources

- **Device Tree**: [GitLab (`fox_12.1-R`)](https://gitlab.com/atsauban/recovery_device_xiaomi_mi439)
- **Test Suite Logs**: [GitLab Logs](https://gitlab.com/atsauban/recovery_device_xiaomi_mi439/-/tree/logs)
- **Releases**: [GitHub Releases](https://github.com/atsauban/OrangeFox-mi439/releases)
