# 🌐 LinguaLocal

> **Live like a local.**

LinguaLocal is a zero-backend, single-file Progressive Web App (PWA) for learning a new language the way expats actually need it — phrases for housing, utilities, transport, and daily life. Built with Claude AI, deployed on Vercel, installable on any device with no App Store required.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-lingua--local.vercel.app-0f0e17?style=for-the-badge&logo=vercel&logoColor=e8a045)](https://lingua-local-wfkr.vercel.app)
[![PWA Ready](https://img.shields.io/badge/PWA-Installable-8b5cf6?style=for-the-badge&logo=pwa&logoColor=white)](https://lingua-local.vercel.app)
[![Built with Claude](https://img.shields.io/badge/Built%20with-Claude%20AI-e8a045?style=for-the-badge)](https://anthropic.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-fffffe?style=for-the-badge)](LICENSE)

---

## ✨ Features

### 🗣️ 12 Supported Languages
English · Spanish · French · Japanese · Italian · German · Portuguese · Mandarin · Arabic · Cantonese · Thai · Vietnamese

Switching languages re-renders the **entire app instantly** — every greeting, phrase, challenge, and AI coach response updates in real time.

---

### 📱 9 App Screens

| Tab | Description |
|-----|-------------|
| **Home** | Personalized greeting, daily challenge, streak tracker, stats cards, and an emergency SOS mode with survival phrases |
| **Phrases** | Category-organized phrases (Housing, Food, Transport, Emergency, and more) with native script, romanization, and one-tap TTS |
| **Write** | Type translations with a special character keyboard, hints, and audio prompts |
| **Speak** | Record yourself, compare against a native speaker, and get a live accuracy/fluency/intonation score |
| **Translate** | Two-way text and voice translation between any supported languages with a live conversation mode |
| **📷 Visual** | Point your camera at a menu, sign, or document — Claude AI extracts and translates all visible text instantly |
| **Currency** | Live exchange rates (refreshed every 10 min), quick-amount buttons, a built-in calculator, and local cost-of-living context |
| **Coach** | AI conversation partner (Sofia, Hana, Linh, Claire, and more) powered by Claude, focused on expat daily life scenarios |
| **Progress** | 14-day words-learned chart, skill breakdown bars, GitHub-style activity heatmap, and milestone achievements |

---

### 🔌 Full Offline Support

LinguaLocal is built to work **without a connection**:

- **Cache-First strategy** for the app shell (HTML, fonts, Chart.js)
- **All phrase data pre-cached** at service worker install — Phrases, Home, Write, and Speak screens are 100% functional offline
- **Offline banner** (amber) appears automatically and dismisses when connectivity returns
- **Last-cached exchange rates** displayed with a timestamp when the currency API is unreachable
- **Network-First with graceful fallback** for Claude AI features — a friendly message replaces broken states
- All LocalStorage data (streak, progress, saved phrases, selected language) persists fully offline

---

### ⚙️ Technical Highlights

- **Zero backend** — single `index.html` file, no build tools, no dependencies to install
- **PWA manifest** embedded as a data URI — installable on iOS and Android from the browser
- **Service Worker** registered via Blob URL (no separate SW file needed)
- **Web Speech API** for text-to-speech and voice recognition across all screens
- **MediaRecorder API** for in-app recording on the Speak screen
- **Claude API** (`claude-sonnet-4-20250514`) powering the AI Coach and Visual Translate features
- **Chart.js** (via CDN) for the Progress screen visualizations
- **LocalStorage** for streak data, progress stats, saved phrases, and language persistence across reloads
- Full error handling and loading states on all API calls

---

### 🎨 Design System

```css
--bg:           #0f0e17   /* Deep dark base */
--surface:      #1a1928   /* Card background */
--surface2:     #252438   /* Elevated surface */
--border:       rgba(255,255,255,0.08)
--accent:       #e8a045   /* Gold — primary actions */
--accent2:      #8b5cf6   /* Purple — interactive elements */
--text:         #fffffe
--text-muted:   rgba(255,255,255,0.5)
```

- **Fonts:** Playfair Display (headings, numbers) + DM Sans (body)
- **Mobile-first** — fixed top header + bottom tab nav with `env(safe-area-inset-bottom)` support
- **Desktop (768px+)** — left sidebar with logo, language selector, nav, and streak counter
- All touch targets minimum 44px with `:active` feedback states

---

## 🚀 Deployment

This project auto-deploys to Vercel on every push to `main`.

```bash
# Clone the repo
git clone https://github.com/your-username/lingua-local.git

# That's it — open index.html in a browser
# or drop the repo into Vercel for instant deployment
```

No `npm install`. No build step. Drop and deploy.

---

## 📲 Install as a PWA

1. Open [lingua-local.vercel.app](https://lingua-local.vercel.app) in Safari (iOS) or Chrome (Android)
2. Tap **Share → Add to Home Screen** (iOS) or the **Install** prompt (Android/Chrome)
3. Launch from your home screen — it runs like a native app, offline included

---

## 🧠 AI Features

### Visual Translate
Upload a photo or open your camera. LinguaLocal sends the image to Claude and returns:
- Extracted original text
- Full translation in your selected language
- Context note (e.g., "This is a lease clause," "This is a restaurant menu")

Translated text can be read aloud via TTS, saved to your phrase list, or shared via the Web Share API.

### AI Language Coach
A named conversation partner responds in your target language with English translations shown below each message. Context is optimized for **relocation and expat daily life** — not tourist small talk.

Coach names by language: Sofia (Spanish) · Hana (Japanese) · Linh (Vietnamese) · Claire (French) · Marco (Italian) · and more.

---

## 🗺️ Roadmap

- [ ] Cloud sync / user accounts
- [ ] Community-contributed expat phrases
- [ ] Apple App Store + Google Play submission
- [ ] Monetization (post-audience validation)
- [ ] Offline mode improvements (background sync)

---

## 🛠️ Built With

- [Claude AI](https://anthropic.com) — AI Coach + Visual Translate
- [Vercel](https://vercel.com) — Hosting & auto-deployment
- [Chart.js](https://chartjs.org) — Progress visualizations
- [Web Speech API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API) — TTS & voice recognition
- [Open Exchange Rates](https://openexchangerates.org) — Live currency data

---

## 📄 License

MIT © [Satori Sojourner](https://github.com/your-username)

---

<p align="center">
  Built for the expat who's done relying on Google Translate screenshots.<br/>
  <strong>Live like a local.</strong>
</p>
