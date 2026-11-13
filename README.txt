# Oromia Social Android starter

This is an Android Studio project wrapper for the Oromo-language HTML prototype.

## Build an APK
1. Download and unzip `OromiaSocialAndroid.zip` on a computer.
2. Install Android Studio and a compatible JDK (Android Studio's bundled JDK is recommended).
3. In Android Studio, choose **Open** and select the extracted `OromiaSocialAndroid` folder.
4. Allow Gradle sync. If prompted, install Android SDK Platform 35 and Build Tools.
5. Choose **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
6. When the build finishes, use the **locate** link in Android Studio. The debug APK is usually at:
   `app/build/outputs/apk/debug/app-debug.apk`
7. Transfer the APK to your Android phone and open it. Only install APKs from sources you trust.

## Important limitations
- This project wraps the prototype in an Android WebView; it is not a production social network.
- Login is only a local demo; never use a real password.
- Uploaded media is only shown locally during the session and is not sent to a server.
- A production release needs secure authentication, backend/database, cloud media storage, moderation/report/block tools, privacy policy, and testing.
- The project folder is source code, not a compiled APK. A build environment is needed to produce the APK.

## Build APK from your phone using GitHub Actions (cloud build)
1. On your phone, download this ZIP and extract it using a trusted archive/file manager.
2. Create/sign in to a GitHub account at https://github.com.
3. Create a new repository, e.g. `OromiaSocialAndroid`.
4. Upload the *contents* of this project folder (including the hidden `.github/workflows/android.yml` file). If uploading from the GitHub web UI does not include hidden files, use GitHub's web editor to create `.github/workflows/android.yml` and paste the workflow content from this project.
5. Open the repository's **Actions** tab and run **Build Oromia Social APK** (or push to `main`).
6. When the workflow completes, open the run, download artifact `Oromia-Social-debug-APK`, extract it, and install `app-debug.apk` on your phone.
7. Use only repositories you control; do not upload passwords or private keys.

Cloud build needs GitHub sign-in and internet. The produced debug APK is for testing, not Play Store publication.
