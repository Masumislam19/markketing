# DroidGuide Notes — Starter Website (বাংলা নির্দেশিকা)

এটি একটি static website starter: HTML + CSS + JavaScript। কোনো paid theme, build tool, database, API key বা backend দরকার নেই।

## ১) লোকালি চালাও

1. ZIP extract করো।
2. `index.html` ডাবল-ক্লিক করে browser-এ খোলো।
3. আরও ভালো local preview-এর জন্য VS Code-এ folder খোলো এবং Live Server extension ব্যবহার করো; অথবা Python থাকলে folder-এর ভেতর terminal থেকে `python -m http.server 8000` চালিয়ে `http://localhost:8000` খোলো।

## ২) প্রকাশের আগে নিজের তথ্য বসাও

- সব পেজে `DroidGuide Notes` ব্র্যান্ড নাম পরিবর্তন করতে পারো। নামটি ব্যবহার করার আগে trademark/handle/domain availability নিজে যাচাই করো।
- `contact.html`-এ `hello@YOUR-DOMAIN.com`-কে নিজের নিয়ন্ত্রণে থাকা ইমেইল দিয়ে বদলাও।
- `sitemap.xml`-এ `https://YOUR-SITE-URL/`-এর সব উদাহরণ তোমার live URL দিয়ে বদলাও।
- `robots.txt`-এর sitemap comment-ও live sitemap URL দিয়ে বদলাতে পারো।
- About, Privacy ও Affiliate Disclosure পেজ নিজের বাস্তব কাজের সঙ্গে মিলিয়ে আপডেট করো।
- Google Support-এর বাইরের লিংকগুলো প্রকাশের আগে খুলে যাচাই করো।

## ৩) GitHub Pages-এ ফ্রি deploy

1. GitHub account-এ sign in করো: https://github.com/
2. New repository তৈরি করো। Public রাখলে GitHub Free-তে Pages ব্যবহার করা যায়।
3. এই project-এর **ভেতরের সব ফাইল ও folder** repository-র root-এ upload করো; অর্থাৎ `index.html` root-এ থাকতে হবে, zip ফাইলের ভেতরে অতিরিক্ত parent folder যেন না থাকে।
4. Repository → Settings → Pages-এ যাও।
5. Build and deployment → Source-এ `Deploy from a branch` বেছে নাও।
6. Branch `main`, folder `/ (root)` বেছে Save করো।
7. কিছুক্ষণ পরে Pages settings-এ live URL দেখাবে।

GitHub-এর official quickstart: https://docs.github.com/en/pages/quickstart

## ৪) Cloudflare Pages-এ বিকল্প ফ্রি deploy

1. https://dash.cloudflare.com/ এ account খোলো।
2. Workers & Pages → Create application → Pages-এ যাও।
3. Git repository connect করে GitHub repo select করো।
4. Framework preset: None; Build command খালি; Build output directory `/` বা project root (Cloudflare UI যেটি চায়) সেট করো।
5. Deploy করো। Dashboard তোমাকে একটি `*.pages.dev` ঠিকানা দেবে। UI পরিবর্তিত হলে Cloudflare-এর বর্তমান documentation অনুসরণ করো: https://developers.cloudflare.com/pages/

## ৫) CPAGrip-এর জন্য গুরুত্বপূর্ণ

এই starter free hosting-এর subdomain-এ publish করা যায়। কিন্তু CPAGrip-এর বর্তমান Terms অনুযায়ী Affiliate approval-এর জন্য reviewed/approved, content-based, fully functional website এবং top-level domain প্রয়োজন। `github.io` বা `pages.dev` subdomain নিজে top-level domain নয়। তাই free preview site-কে approval নিশ্চিত ধরে নিও না। CPAGrip Support-কে জিজ্ঞেস করো; TLD দরকার হলে domain কেনার আগে approval/requirements নিশ্চিত করো।

Official Terms: https://www.cpagrip.com/terms.php

ওয়েবসাইটে এখন কোনো affiliate/CPA link নেই। Approval ও campaign-specific written rules না পাওয়া পর্যন্ত CPA link বসিও না। কোনো fake signup, self-conversion, bot, incentivized traffic, forced redirect, misleading claim বা spam ব্যবহার কোরো না।

## ৬) SEO ও quality checklist

- প্রতিটি article নিজে পড়ে যাচাই ও প্রয়োজনমতো rewrite/expand করো।
- নিজের real screenshots যোগ করো; private notification, account, phone number বা personal data দেখা যাবে না।
- প্রতিটি নতুন article-এ unique title, description, headings, internal links এবং trusted primary sources রাখো।
- Search Console-এ site verify করার পর sitemap submit করতে পারো।
- Broken links, mobile layout, page speed, spelling এবং contact details পরীক্ষা করো।
- Privacy policy-তে analytics, ads, embeds, forms বা tracking যোগ করলে সেগুলো সত্যভাবে disclose করো।

## ৭) ভিডিও workflow (তোমার PC-তে)

### Android screen demo কীভাবে করবে
- যদি নিজের Android ফোন ব্যবহার করতে পারো, ফোনের built-in Screen Recorder দিয়ে demo record করে USB বা trusted file transfer দিয়ে PC-তে আনো। Notification ও ব্যক্তিগত তথ্য লুকিয়ে রাখো।
- ফোন না থাকলে Android Studio-এর Android Emulator দিয়ে PC-তে virtual Android device চালাতে পারো: https://developer.android.com/studio/run/emulator । Android Studio download: https://developer.android.com/studio । Device Manager থেকে Create Device → device profile → system image → Finish করে emulator চালাও। Google-এর best-experience requirement হিসেবে 16 GB RAM ও 16 GB disk উল্লেখ আছে; কম spec-এ emulator ধীর হতে পারে। Emulator আসল ফোন নয়—ভিডিওতে “emulator demo” হিসেবে পরিচয় দেবে এবং কেবল তুমি নিজে যাচাই করা screen দেখাবে।
- Emulator/PC window capture করতে OBS Studio ব্যবহার করো: https://obsproject.com/download ।

### Free/Free-to-start tools
- OBS Studio — PC/emulator window record: https://obsproject.com/download
- Clipchamp — PC editing; Free plan-এ 1080p export ও watermark-free video আছে, Premium stock/assets আলাদা: https://clipchamp.com/en/pricing/
- DaVinci Resolve — advanced editing; Free edition আছে: https://www.blackmagicdesign.com/products/davinciresolve
- Canva — thumbnails/graphics; free plan-এ সব asset নয়: https://www.canva.com/
- Audacity — voice cleanup: https://www.audacityteam.org/
- YouTube Audio Library — music/sound: https://www.youtube.com/audiolibrary (প্রতিটি track-এর license terms যাচাই করো)।

### 4-hour daily process
1. 30 min: একটি নির্দিষ্ট প্রশ্ন/সমস্যা বাছাই এবং Android/Google-এর official docs যাচাই।
2. 45 min: 100–140 শব্দের script লেখা; প্রথম 2 seconds-এ প্রশ্ন বা ফলাফল, তারপর 3টি ধাপ, শেষে natural follow CTA।
3. 45 min: নিজের ফোন বা emulator-এ settings/demo record; personal data hide করো।
4. 60 min: edit, readable captions, clean audio, export vertical 1080x1920।
5. 30 min: YouTube Shorts, TikTok, Facebook Reels-এ platform-specific caption দিয়ে publish (প্রতিটি platform-এর link/promotion policy মানো)।
6. 30 min: comments, retention, saves, clicks/website analytics নোট করো।

### প্রথম 7টি ভিডিওর বিষয় ও hook
1. “How to check app permissions on Android” — camera, mic, location permissions কোথায় দেখা যায়।
2. “Find the apps using the most battery” — Battery usage screen দেখাও।
3. “Free up storage without deleting important files” — Downloads/large files যাচাই।
4. “What does ‘Clear cache’ actually do?” — cache বনাম clear storage/data আলাদা বোঝাও।
5. “Turn off notifications from one noisy app” — app notification settings দেখাও।
6. “Find your Android version in seconds” — About phone/Android version location দেখাও।
7. “Three checks before installing an unfamiliar app” — developer, permissions, reviews/official store page যাচাই।

প্রতিটি ভিডিওতে নিজের demo/voiceover ব্যবহার করো। অন্যের ভিডিও, music, logo, screenshot বা article কপি কোরো না। ভুল তথ্য দিয়ে download/registration করাতে চেষ্টা কোরো না।

## ৮) CPA link বসানোর আগে

1. CPAGrip-এর approval নাও এবং exact media/site approve করাও।
2. Offer-এর GEO, device, allowed traffic sources, incentive rules, payout conditions পড়ো।
3. Social traffic অনুমোদিত না হলে social থেকে CPA link পাঠিও না।
4. Link-এর পাশে clear disclosure দাও।
5. শুধু genuine user action; নিজের offer নিজে complete, bot, proxy, fake lead, forced click নয়।
6. Net terms, payout threshold, tax form এবং Bangladesh payout method Support থেকে নিশ্চিত করো।

---

This is a starter template, not a guarantee of search ranking, network approval, conversions, or income. Review all content, links, privacy disclosures, and platform rules before launch.
