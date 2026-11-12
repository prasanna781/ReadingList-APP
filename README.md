# Reading List (Android, Kotlin)

Add books by scanning an ISBN barcode (EAN-13 only) or by searching a title, then track
reading status (Want to read / Reading / Finished). Login with Firebase Authentication,
books stored in Firestore under `users/{uid}/books/{isbn}`.

## Before you run (2 minutes)

1. Create a Firebase project: https://console.firebase.google.com
2. Add an Android app with package name `com.example.readinglist`
3. Download `google-services.json` and put it inside the `app/` folder
   (next to `app/build.gradle.kts`). The build fails without it.
4. In the Firebase console:
   - Authentication > Sign-in method > enable **Email/Password**
   - Firestore Database > Create database > start in **test mode**

## Run

1. Android Studio > File > Open > select this `ReadingList` folder
2. Wait for Gradle sync to finish
3. Run on a real phone, or an emulator that has Google Play (Play Store image).
   The Google code scanner needs Google Play services.

## Notes

- Use JDK 17 (Android Studio > Settings > Build > Gradle > Gradle JDK).
- First scan may say the scanner module is downloading. Wait a few seconds and retry.
- If Firestore says "permission denied", your test-mode rules expired (30 days).
  Recreate the rules or the database.
