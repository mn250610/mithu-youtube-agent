# Mithu YouTube Agent — Android APK 1.0.0

এটি একটি Android WebView অ্যাপের প্রাথমিক ভিত্তি। এতে Dashboard, Manual Approval/Auto Upload mode switch এবং স্থানীয় Settings সংরক্ষণের UI আছে।

## গুরুত্বপূর্ণ সীমাবদ্ধতা
এই build-এ এখনো AI story generation, Bengali TTS, video rendering, Google OAuth, YouTube upload বা Analytics API সংযুক্ত নেই। UI-তে এগুলোকে প্রস্তুত/সংযুক্ত বলে দাবি করা হয়নি। বাস্তব আপলোডের আগে Google OAuth consent, YouTube Data API এবং প্রয়োজনীয় অনুমতি লাগবে। Google পাসওয়ার্ড কখনো অ্যাপে সংগ্রহ করবেন না।

## GitHub দিয়ে APK বানানো (Android ফোন থেকে)
1. GitHub-এ নতুন Public বা Private repository তৈরি করো, যেমন `mithu-youtube-agent`।
2. এই ZIP ফাইলটি Extract করো।
3. Extract করা ফোল্ডারের ভেতরের `settings.gradle`, `build.gradle`, `gradle.properties`, `app` ফোল্ডার ইত্যাদি repository-র root-এ Upload files দিয়ে আপলোড করো।
4. পরের ধাপে দেওয়া `build-apk.yml` ফাইলের কনটেন্ট GitHub-এ `.github/workflows/build-apk.yml` নামে নতুন ফাইল হিসেবে তৈরি করো।
5. Commit changes করো। GitHub Actions স্বয়ংক্রিয়ভাবে APK build করবে।
6. Repository → Actions → সর্বশেষ সফল workflow → Artifacts থেকে `MithuYouTubeAgent-debug-apk` ডাউনলোড করো।
7. ZIP extract করে APK ইনস্টল করো। ফোনে “Install unknown apps” অনুমতি চাইতে পারে।

## Build details
- Android application ID: `com.mithu.youtubeagent`
- Version: `1.0.0` (versionCode 1)
- Minimum Android: 6.0 (API 23)
- Compile/Target SDK: 35
- JDK: 17
