# SPLOSH — Offline Translator (starter)

SPLOSH is an Android starter project for an offline-first multilingual translator.

## Current starter features
- Arabic-first dark interface.
- 59 language choices presented in the UI.
- On-device text translation through Google ML Kit Translation.
- Translation model download on first use; after the required model is downloaded, translation can work offline.
- Copy, clear, and basic local translation history storage.
- GitHub Actions workflow that builds a debug APK.

## Important language coverage note
The UI list contains 59 language choices, matching the ML Kit language list documented for this engine, but the ML Kit translation engine is the actual authority for language availability. The first release does **not** claim support for every language in the world. Verify every pair on-device. Some language pairs may route through English, which can affect quality.

## First run
1. Connect the phone to the internet.
2. Choose source and target languages.
3. Connect to Wi-Fi and translate once so ML Kit can download the required models.
4. Keep the models on the device; later translations can run offline.
5. Use Wi-Fi for model downloads when possible. Model downloads use device storage.

## Build with GitHub Actions
1. Create a new GitHub repository named `SPLOSH`.
2. Upload the contents of this folder to the repository's `main` branch.
3. Open the **Actions** tab.
4. Run **Android Debug APK** (or push a commit).
5. Open the successful workflow run and download the `SPLOSH-debug-apk` artifact.

The APK is a debug build for testing, not a signed Play Store release.

## Build locally
Requires JDK 17, Android SDK platform 36, and Gradle 8.13:
```bash
gradle assembleDebug
```

## Planned next stages
Conversation mode, camera OCR, document/PDF translation, speech input/output, SRT tools, contextual alternatives, grammar correction, dictionary, advanced language packs, and SPLOSH LAB are planned but are not implemented in this starter.
