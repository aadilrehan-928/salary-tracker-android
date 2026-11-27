# My Salary Tracker — Android project

This Android Studio project wraps the existing Salary Tracker web app in an Android WebView. The app assets are bundled locally; the salary/expense records remain in WebView IndexedDB on this device.

## Build an APK with Android Studio
1. Install Android Studio (current stable) and the Android SDK Platform 35.
2. Extract this project ZIP.
3. In Android Studio choose **Open** and select the extracted `salary-tracker-android` folder.
4. Allow Gradle sync and install any SDK components Android Studio requests.
5. Select **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
6. The debug APK is created at `app/build/outputs/apk/debug/app-debug.apk`.
7. Transfer the APK to your Android phone and install it. If prompted, allow installation from that file manager/browser.

## Build from command line
With JDK 17 or newer, Android SDK and Gradle 8.9 installed:

```bash
gradle assembleDebug
```

## Features
- Offline bundled web application
- IndexedDB local data storage
- Four-digit PIN lock
- Salary, allowances, deductions and expenses
- Monthly dashboard and reports
- CSV and JSON backup files saved to Downloads/SalaryTracker
- Android system print dialog for PDF output

## Notes
- No network permission is requested. The app is designed to work offline.
- Data is local to this app installation and is not synchronized to other devices.
- Uninstalling the app or clearing its app data can delete records. Export a JSON backup regularly.
- The PIN is a local app lock, not encryption of the IndexedDB database. Protect the Android device with its own screen lock.
- The APK has not been compiled or device-tested in this environment; use Android Studio to build and test it.
