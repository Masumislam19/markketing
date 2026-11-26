# RewardPath Guide — বাংলা Setup Guide

এই প্রজেক্টটি **Astro 6 (Node.js-powered static site generator)** দিয়ে তৈরি। এটি Express/Node server নয়। লোকাল PC-তে Node.js দিয়ে build ও preview করবে; GitHub Pages-এ শুধু static HTML/CSS/JS প্রকাশ হবে।

## তোমার PC-তে যা আছে

তুমি জানিয়েছ:

- Node.js: `v22.22.0`
- npm: `10.9.4`

এই প্রজেক্টে Astro `6.4.6` pin করা আছে, যার জন্য Node `22.12.0+` দরকার। তোমার Node version যথেষ্ট। Astro 7-এর সাম্প্রতিক রিলিজে Node-এর আরও নতুন patch version লাগতে পারে, তাই আপাতত Astro 6 ব্যবহার করছি।

## Step 1 — VS Code-এ Open

1. ZIP Extract করো।
2. VS Code → File → Open Folder → `rewardpath-github-pages-starter` folder নির্বাচন করো।
3. Terminal → New Terminal খোলো।

## Step 2 — Dependency Install

```powershell
npm install
```

প্রথমবার internet লাগবে। এতে `node_modules` এবং `package-lock.json` তৈরি হবে।

## Step 3 — Local Website চালাও

```powershell
npm run dev
```

Terminal-এ যে address দেখাবে (সাধারণত `http://localhost:4321/`) সেটি browser-এ খোলো।

## Step 4 — Production Build পরীক্ষা

Dev server বন্ধ করতে Terminal-এ `Ctrl + C` চাপো, তারপর:

```powershell
npm run build
npm run preview
```

Preview URL Terminal-এ দেখানো হবে। `astro.config.mjs`-এ `base: '/markketing'` দেওয়া আছে, কারণ GitHub Pages URL হবে:

`https://masumislam19.github.io/markketing/`

## গুরুত্বপূর্ণ পরিবর্তন করার জায়গা

- `src/pages/contact.astro`: placeholder email বদলে নিজের email বসাও।
- `src/pages/privacy.astro`: analytics/cookies যোগ করলে policy আপডেট করবে।
- `src/data/guides.js`: article content বদলাবে/নতুন guide যোগ করবে।
- `astro.config.mjs`: GitHub username বা repository বদলালে `site` ও `base` বদলাতে হবে।
- `public/sitemap.xml` ও `public/robots.txt`: production URL পরিবর্তন হলে আপডেট করবে।

## GitHub Pages-এ পরে Deploy

এই project-এ `.github/workflows/deploy.yml` আগে থেকেই আছে। এটি Astro-এর official GitHub Action দিয়ে build ও deploy করবে।

GitHub repository-র Settings → Pages → Build and deployment → Source-এ **GitHub Actions** নির্বাচন করতে হবে। তারপর `main` branch-এ project files push করলে Action deploy করবে।

প্রজেক্টে `base: '/markketing/'` রাখা হয়েছে। Repository নাম `markketing` থাকলেই এটি সঠিক।

Push করার আগে `npm install` চালিয়ে তৈরি হওয়া `package-lock.json` commit করবে। `node_modules` ও `dist` push করার দরকার নেই।

## Content ও CPA সতর্কতা

সাইটে কোনো অনুমোদনহীন CPA link নেই। কোনো gift card sweepstakes-কে guaranteed prize হিসেবে বলা হয়নি। CPAGrip থেকে লিখিত অনুমোদন, নির্দিষ্ট offer availability, GEO এবং traffic-source permission নিশ্চিত না হওয়া পর্যন্ত offer link বসাবে না।

Contact page-এর placeholder email প্রকাশের আগে বদলাবে। এই starter policy pages তোমার বাস্তব data collection/hosting সেটিংসের সঙ্গে মিলিয়ে নিতে হবে।
