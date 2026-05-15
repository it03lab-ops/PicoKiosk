# PicoKiosk

**Kiosk-mode launcher for PICO 4 (and possibly Meta Quest) VR headsets**  
Based on [PicoZen](https://github.com/barnabwhy/PicoZen) by [barnabwhy](https://github.com/barnabwhy), with major modifications for restricted public use.

> ⚠️ **Unofficial project** – not affiliated with PICO or Meta.  
> ✅ Designed for scenarios where a VR headset is shared by multiple users (museums, showrooms, training, etc.).  
> 🔒 Locks the user into approved apps only – no access to system settings, home button, notification bar.

---

## 🎯 Features (vs original PicoZen)

| Feature | PicoZen (original) | PicoKiosk (this fork) |
|---------|--------------------|------------------------|
| Show all installed apps | ✅ | ❌ (whitelist only) |
| Admin-controlled app whitelist | ❌ | ✅ |
| Block system settings access | ❌ | ✅ |
| Block notification bar / quick settings | ❌ | ✅ |
| Prevent exit to system launcher (HOME button) | ❌ | ✅ |
| Sideloading APKs | ✅ | ✅ (optional, can be disabled) |

---

## ⚠️ Compatibility & Caveats

- **Primary target:** PICO 4 (tested on PICO 4). Should work on PICO Neo 3.
- **Meta Quest (Quest 2/3/Pro):** *Untested.* Because the original PicoZen was reported to work on Quest, this fork may also run on Quest, but **no guarantees**. The system UI blocking methods differ between PICO and Meta’s VROS. Use at your own risk.
- **Android version requirement:** Android 10+ (typical for XR headsets).

---

## 📥 Installation

1. **Download the latest APK** from [Releases](#) (not yet available – you will build from source).
2. **Sideload the APK** onto your headset (using ADB or SideQuest).
3. **Launch PicoKiosk** from the system launcher.
4. **Grant overlay / notification permissions** if requested.
5. **Set PicoKiosk as default launcher** (may require ADB: `adb shell pm set-home-activity com.yourname.picokiosk/.MainActivity`).

---

## 🔧 Building from source

```bash
git clone https://github.com/it03lab-ops/PicoKiosk.git
cd PicoKiosk
# Open in Android Studio, sync Gradle, then Build -> Build APK(s)


