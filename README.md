# ClipGenius AI — Ssemble-inspired MVP

This package is an expanded starter implementation, not a complete feature-for-feature Ssemble clone.

## Included in this build
- YouTube URL input and local video upload
- Speech-to-text transcription with Faster-Whisper
- Basic transcript-density/keyword highlight ranking
- Adjustable clip duration (15–90 sec) and count (1–10)
- 9:16, 1:1 and 16:9 export
- Selectable subtitle looks
- MP4 export and suggested clip titles
- Android WebView wrapper and GitHub Actions APK build workflow

## Not yet implemented
Commercial-level semantic highlight understanding, face/speaker tracking, word-by-word animated captions, templates/brand kits, stock footage, music catalog, multi-track editor, team collaboration, publishing/scheduling, analytics, account system, and scalable job queue/storage. Those need separate design, APIs, testing and potentially paid services.

## Deploy the server
Create a Gradio Space on Hugging Face. Upload `server/app.py`, `server/requirements.txt`, and `server/packages.txt` to the Space root. Wait for it to build. Copy its public HTTPS URL.

## Build Android APK
1. Create a GitHub repository.
2. Upload the complete extracted project folder contents, including hidden `.github` folder and workflow.
3. Open Actions and run **Build ClipGenius AI APK**.
4. Download the artifact named `ClipGenius-AI-debug-apk`.
5. Extract the artifact ZIP; install `app-debug.apk` on Android.
6. Enter your Hugging Face Space URL in the app and open the studio.

## Upload files to GitHub from Android
1. Download the project ZIP and extract it with Files by Google or another archive app.
2. In Chrome, open GitHub and create a new repository named `clipgenius-ai`.
3. In the repository, use **Add file → Upload files**.
4. Upload the extracted files and folders. Ensure `.github/workflows/build-apk.yml` is included. If the mobile upload UI cannot upload nested folders or hidden files, use GitHub's web editor to create `.github/workflows/build-apk.yml`, or use GitHub's mobile app/desktop site.
5. Commit the files to the `main` branch.
6. Go to **Actions**, enable workflows if prompted, select **Build ClipGenius AI APK**, and tap **Run workflow**.
7. Wait for a green check. Open the completed run, find Artifacts, and download `ClipGenius-AI-debug-apk`.
8. Extract the downloaded artifact and install the APK. Android may ask you to allow installs from Chrome/Files.

## Android APK notes
This project builds a debug APK using GitHub Actions and Gradle. It is not a signed Play Store release. A public HTTPS processing server is required. Free hosting has CPU, memory, file-size, sleeping and runtime limitations. This is not offline/on-device AI.

## Responsible use
Use only videos you own or have permission to download and edit. Respect copyright, platform terms, privacy, and applicable law. The app cannot bypass private, members-only, age-restricted, DRM-protected or other access controls.
