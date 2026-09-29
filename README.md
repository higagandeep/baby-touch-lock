<p align="center">
  <img src="ic_launcher-playstore.png" width="128" height="128" alt="Baby Touch Lock Logo" />
</p>

<h1 align="center">Baby Touch Lock 🔒👶</h1>
<p align="center"><strong>A Parent Survival Tool</strong></p>

<p align="center">
  <a href="https://f-droid.org/packages/com.babytouchlock/"><img src="https://img.shields.io/f-droid/v/com.babytouchlock?logo=fdroid" alt="F-Droid" /></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-GPLv3-blue.svg" alt="License: GPL v3" /></a>
  <a href="https://android.com"><img src="https://img.shields.io/badge/Platform-Android%208.0%2B%20(API%2026%2B)-green.svg" alt="Platform" /></a>
  <a href="PRIVACY_POLICY.md"><img src="https://img.shields.io/badge/Permissions-Zero%20Internet-brightgreen.svg" alt="No Internet" /></a>
</p>

---

## 🍼 Why Baby Touch Lock?

Every parent knows the scene: you hand your phone to your toddler so they can watch their favorite cartoon or video clip in peace while you catch your breath. 

**3 seconds later:**
- 💥 The video is closed.
- 📞 You are accidentally video-calling your boss on WhatsApp.
- 📦 40 items have been added to your shopping cart.
- 💔 You've accidentally liked a post from your ex.
- 🔊 The volume is blasted to 100% or muted completely.
- 😭 A meltdown of biblical proportions begins because *“the cartoon went away!”*

Tiny toddler hands love holding the screen by the edges, tapping everywhere, swiping home, and mashing the volume buttons.

**Baby Touch Lock** was created to restore peace and sanity. With a single tap from your Quick Settings, it puts an invisible, impenetrable barrier over your screen. Your kid can safely grip the phone with both hands, tap like a maniac, and enjoy their show without interrupting playback or compromising your digital life.

---

## ✨ Key Features

- **Full Screen Touch Blocking**: Prevents inadvertent taps, swipes, and pinches while watching media.
- **Edge & Gesture Navigation Neutralization**: Overrides edge back swipes, Home gesture, and App Switch gestures via modern Android Insets & Exclusion APIs.
- **Notification Shade Guard**: Prevents the status bar and Quick Settings shade from being pulled down during playback.
- **Physical Volume Lock**: Suppresses hardware volume buttons to prevent sudden volume spikes (or accidental mutes).
- **Instant Screen Wake on Power Button**: Automatically turns the screen back on if the power button is accidentally pressed.
- **Quick Settings Tile**: Fast 1-tap activation right from the Android notification drawer.
- **Child-Proof Unlock Slider**: Vertical slide-to-unlock mechanism placed out of the way to prevent accidental unlocking by children.
- **100% Offline & Private**: Zero network permissions, zero tracking, zero analytics, zero ads.

---

## 📥 Download

Install from **F-Droid** (recommended for automatic updates) or download the latest standalone APK directly from GitHub **[Releases](https://github.com/dmici/baby-touch-lock/releases)**.

<p align="center">
  <a href="https://f-droid.org/packages/com.babytouchlock/">
    <img src="https://fdroid.gitlab.io/artwork/badge/get-it-on.png"
         alt="Get it on F-Droid"
         height="80">
  </a>
</p>


---

## 🚀 How to Use

1. **Grant Accessibility Permission**:
   - Open **Baby Touch Lock**.
   - Tap **Enable Service** to open Android Settings and enable **Baby Touch Lock Service** under **Accessibility**.
2. **Add Quick Settings Tile**:
   - Tap the **Add** button in the **Quick Settings** section.
   - Swipe down twice from the top of your screen to expand the Quick Settings panel.
   - Tap the pencil icon ✏️.
   - Find the **Baby Lock** tile and drag it to your active tiles.
3. **Lock & Unlock**:
   - **To Lock**: Start any video or cartoon, pull down your notification tray, and tap the **Baby Lock** tile. The screen, gestures, volume keys, and notification shade are now securely locked.
   - **To Unlock**: Firmly slide the vertical unlock handle upwards to disengage the lock.

---

## 🛠️ Build

### Compatibility & Requirements
- **Supported Devices (Runtime)**: Android 8.0+ (API level 26+)
- **Build Requirements**:
  - Android SDK (API 36 / `compileSdk = 36`)
  - JDK 17+
  - Gradle 8.4+ (included via wrapper)

### Building from Source

To build a debug APK locally (no signing keystore required):
```bash
./gradlew assembleDebug
```
The resulting APK will be placed in `app/build/outputs/apk/debug/app-debug.apk`.

---

## 🔒 Permissions Explained

| Permission | Purpose |
| :--- | :--- |
| `BIND_ACCESSIBILITY_SERVICE` | Used to filter touch events, navigation bar gestures, and hardware keys while the lock overlay is engaged. Does **not** read screen contents (`canRetrieveWindowContent="false"`). |
| `BIND_QUICK_SETTINGS_TILE` | Exposes the quick toggle shortcut in the Android quick settings drawer. |
| `VIBRATE` | Provides haptic feedback when the screen is unlocked. |
| `WAKE_LOCK` | Briefly wakes the screen if the Power Wake option is enabled. |
| **`INTERNET`** | **NOT REQUESTED.** The app cannot access the network. |

---

## 📜 Privacy Policy & License

- **Privacy Policy**: Read the [Privacy Policy](PRIVACY_POLICY.md).
- **License**: Distributed under the terms of the [GNU General Public License v3.0 (GPL-3.0)](LICENSE).
