# Suntukan sa Kanto — Phase 1 APK

*Kung hindi madaan sa usapan, suntukan na lang.*

Offline Android build of the Suntukan sa Kanto web game. GitHub Actions builds the APK automatically — no Android Studio needed.

## Paano mag-build
1. Upload all files in this folder to the `main` branch of a GitHub repo (keep the folder structure, including `.github/workflows`).
2. Open the **Actions** tab. The **Build APK** workflow runs on every push (or press **Run workflow**).
3. When it turns green, open **Releases** and download `SuntukanSaKanto-buildN.apk` on your Android phone.

## Paano i-update ang laro
Replace `app/src/main/assets/index.html` with the newest game file and commit. A new build appears in Releases. Because every build is signed with the same key (`app/suntukan.keystore`), it installs over the old one and keeps your saves and combos.

## What phase 1 includes
- Full game, 100% offline (fonts bundled)
- Landscape, full screen, screen stays on
- Back button: pauses the fight / skips a cutscene / returns to the title; exits only from the title
- Saves, unlocks and recorded combos stay on the phone
- "I-load ang combo file" opens the phone's file picker

## Notes
- The signing key in this repo is for sideloading only. For a Play Store release, make a new private key and keep it out of the repo.
- Fonts: Bungee and Rubik, SIL Open Font License (see `assets/fonts`).
