# BTL EPC Ltd — NFA Portal Android WebView Application

A production-ready, native Android WebView wrapper engineered in Kotlin for **`https://nfa.btlepcltd.com/dashboard`**.

## Key Features Included
- **Secure Session & Cookie Persistence**: Uses Android `CookieManager` (`acceptCookie = true`, `acceptThirdPartyCookies = true`) and DOM storage so users stay signed in securely without hardcoding credentials in the APK.
- **Pull-to-Refresh (`SwipeRefreshLayout`)**: Smooth vertical swipe gesture to reload dashboard data.
- **Top Loading Progress Bar**: Material 3 horizontal progress bar (`LinearProgressIndicator`) showing real-time page load progress.
- **NFA Attachment Uploads (`onShowFileChooser`)**: Full support for selecting PDFs, Excel sheets, images, or capturing photos directly from the device camera when submitting or reviewing NFAs.
- **Native PDF & Document Downloads (`DownloadManager`)**: Automatically intercepts file downloads (such as NFA PDF summaries and annexures) and saves them to the Android `Downloads` folder with a system notification.
- **Smart Hardware Back Navigation (`OnBackPressedCallback`)**: Pressing the Android back button navigates backward through the WebView history rather than abruptly exiting the app.
- **Offline Detection & Branded Retry View**: Detects network loss and displays a clean offline card with a one-tap **Retry Connection** button.
- **1-Click Cloud APK Build (`.github/workflows/build-apk.yml`)**: Automatically compiles the installable `.apk` in the cloud using GitHub Actions if you don't want to install Android Studio locally.

---

## Option 1: Build APK in Android Studio (Local)
1. Download and extract `BTL_NFA_Android_WebView_Project.zip`.
2. Open **Android Studio** (Ladybug / Koala or newer) and select **Open**.
3. Choose the extracted `BTL_NFA_Android_WebView_Project` folder and wait for Gradle Sync to finish.
4. In the top menu, click **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. Once complete, click **Locate** in the bottom-right notification to get your installable APK at:
   `app/build/outputs/apk/debug/app-debug.apk`

---

## Option 2: Build APK Automatically Without Installing Android Studio (GitHub Actions)
1. Create a new **Private Repository** on [GitHub](https://github.com/new).
2. Upload all files from the extracted `BTL_NFA_Android_WebView_Project` folder (including the `.github` folder) to the repository.
3. Click the **Actions** tab in your GitHub repository.
4. The **Build Android APK** workflow will run automatically and finish in ~2 minutes.
5. Click the completed workflow run and download **`BTL-NFA-Portal-APK`** under the **Artifacts** section.
