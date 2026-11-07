KAIRO 2K - CyberFace port 2K14 -> 2K20  (Java + Chaquopy)

WHAT THE USER DOES
  1. Open the app, tap SELECT 2K14 IFF.
  2. (optional) choose Output and Skin.
  3. Tap PORT.  The finished IFFs and the log are saved to  Downloads/KAIRO2K.
  The 2K20 base (BASE_SD.iff) is built in:  app/src/main/assets/BASE_SD.iff

PROJECT
  app/src/main/java/com/kairo2k/MainActivity.java   UI (red / black, no AndroidX, no lambdas)
  app/src/main/java/com/kairo2k/ProgressCb.java     progress callback used by Python
  app/src/main/python/cf_port.py                    the port script (v95 + v96 speed-ups)
  app/src/main/python/cfapp.py                      bridge (run / cancel)
  app/build.gradle                                  Chaquopy 17.2: Python 3.12, numpy, scipy, pillow, abi arm64-v8a + x86_64

AIDE
  Open the folder (the one with settings.gradle) as a Gradle project.  AIDE has to run the Chaquopy plugin
  ('com.chaquo.python') - if AIDE refuses the plugin, build in the cloud instead:
  put this folder in a GitHub repo, open Actions > "Build APK" > Run workflow, download the APK artifact.
  (.github/workflows/build-apk.yml)  No PC needed.
