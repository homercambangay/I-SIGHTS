# A to Z Reading Adventure – Android project

## Easiest: build the APK online (no Android Studio)
1. Create a free account at github.com and make a new **private** repository.
2. Upload everything in this folder (keep the `.github` folder and `www/index.html`).
3. Open the repo's **Actions** tab -> "Build Android APK" -> wait ~5 min for the green check.
4. Open that run, download the **AtoZ-Reading-Adventure-apk** artifact, unzip it.
5. Copy `app-debug.apk` to your phone and tap it to install
   (allow "install unknown apps" when asked).

## Or build locally
Needs Node 20+, Java 17, Android Studio.
    npm install
    npx cap add android
    (add RECORD_AUDIO + MODIFY_AUDIO_SETTINGS permissions to android/app/src/main/AndroidManifest.xml)
    npx cap sync android
    npx cap open android      # then Build > Build APK(s)

## Before publishing to Google Play
- Change `appId` in capacitor.config.json to your own (e.g. com.yourname.azreading).
- Make a signed release bundle (AAB) in Android Studio: Build > Generate Signed Bundle.
