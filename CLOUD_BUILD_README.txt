TENDON GLIDING AR — CLOUD APK BUILD
==================================

This project is built on GitHub's hosted runner. You do NOT need Android Studio,
Java, Gradle, or the Android SDK installed on your laptop.

ONE-TIME SETUP
1. Sign in or create a GitHub account at https://github.com
2. Create a new repository. Choose a name such as tendon-gliding-ar.
   For easiest setup, choose Public; do not upload private data.
3. On the repository page choose Add file > Upload files.
4. Extract this ZIP on your computer, open the extracted folder, select all
   files INCLUDING the hidden .github folder, and upload them to the repository.
   If the browser upload does not show .github, create the workflow file manually:
   .github/workflows/build-apk.yml
   Use the contents of that file from this ZIP.
5. Commit the uploaded files to the main branch.
6. Open the repository's Actions tab.
7. Select "Build Tendon Gliding AR APK" and click "Run workflow" if it did not
   start automatically.
8. Wait for the workflow to finish with a green check.
9. Open that completed workflow run. Under Artifacts, download
   "TendonGlidingAR-APK".
10. Extract the downloaded artifact ZIP. It contains app-debug.apk.
    Rename it to TendonGlidingAR.apk if desired, transfer to your phone,
    and install it. Allow installation from your browser/file manager if asked.

IMPORTANT
- GitHub account and internet connection are required.
- GitHub Actions availability/usage depends on GitHub account and repository
  settings/quotas. Public repositories generally have hosted runner access.
- The APK is a debug build, not a Play Store release.
- The first app launch downloads the MediaPipe hand_landmarker.task model.
- This prototype uses approximate pose thresholds and is not clinically validated.
