TENDON GLIDING AR — ANDROID PROJECT
===================================

WHAT THIS BUILDS
- Android camera preview
- MediaPipe hand landmark tracking (one hand)
- Live hand skeleton and fingertip markers
- Five poses: STRAIGHT, HOOK, SHELF, STRAIGHT FIST, FULL FIST
- 3-second hold per correctly detected pose
- One cycle counted only after all five positions complete
- 10-cycle target
- START/PAUSE, NEXT and RESET controls

BUILD ON WINDOWS
1. Install Android Studio.
2. In Android Studio > SDK Manager, install:
   - Android SDK Platform 35
   - Android SDK Build-Tools 35.x
   - Android SDK Command-line Tools
3. Install a 64-bit JDK 17 (Android Studio's bundled JBR is also suitable).
4. Ensure ANDROID_HOME points to your Android SDK, usually:
   %LOCALAPPDATA%\Android\Sdk
5. Double-click BUILD_APK.bat.
6. After a successful build, find:
   APK\TendonGlidingAR.apk

FIRST APP RUN
- Internet is required once to download the MediaPipe hand_landmarker.task model.
- Camera permission is required.
- After model download, hand tracking runs on-device.

IMPORTANT CLINICAL / TECHNICAL LIMITATIONS
- This is an Android port of the supplied Python prototype's approximate joint-angle
  classification thresholds. It is not a clinically validated diagnostic or treatment tool.
- 2D camera landmarks and approximate angles can misclassify poses depending on camera
  angle, lighting, hand size, occlusion and movement.
- The supplied Python reference says 3-second holds; this port preserves that value.
- NEXT is a manual skip and does not increment the cycle counter.
- Test with a real Android phone before any patient-facing use.

PACKAGE: com.sarvesh.tendongliding
MIN ANDROID: 8.0 (API 26)
TARGET SDK: 35
