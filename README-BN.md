# Mithu YouTube Agent v1.1.0

## এই সংস্করণে কাজ করে
- Dashboard এবং আলাদা Settings পেজ
- Manual Approval / Auto Upload mode নির্বাচন ও স্থানীয়ভাবে সংরক্ষণ
- Channel name, দৈনিক Shorts লক্ষ্য, ভিডিও দৈর্ঘ্য
- AI Provider, Model name ও API Key field
- Voice language ও background music preference
- Save Settings / Reload Saved Settings

## এখনো সংযুক্ত নয়
AI API-তে প্রকৃত request, Bengali TTS, video rendering, Google OAuth, YouTube upload ও Analytics। UI-তে API Key field থাকলেও এটি API-তে কল করে না।

## নিরাপত্তা
এই prototype-এ API Key Android WebView localStorage-এ plaintext অবস্থায় সংরক্ষিত হয়। Production API key ব্যবহারের আগে Android Keystore-backed encrypted storage বা backend proxy যোগ করতে হবে। GitHub-এ API key commit করবেন না।

## Build
GitHub Actions workflow `build-apk.yml` ব্যবহার করুন। Android SDK path runner-এর `ANDROID_HOME` environment থেকে নেওয়া হয়।
