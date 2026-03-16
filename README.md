# 🌐 D Lingo — Live Call Translator App

D Lingo is a smart phone calling application that allows two people speaking **different languages** to communicate easily in real time.

## ✨ Features

- 📞 **Dial Pad** — Select country, auto-detect country code, dial any number
- 👥 **Contacts** — Search and call contacts with language detection
- 🕐 **Recent Calls** — View Incoming / Outgoing / Missed calls
- 🌐 **Live Translation** — Real-time Telugu ↔ English (and other languages) during calls
- 🔇 **Call Controls** — Mute, Speaker, Translation ON/OFF

## 🚀 Getting Started

### Prerequisites
- Node.js >= 16
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/dlingo.git

# Go into the project folder
cd dlingo

# Install dependencies
npm install

# Start the app
npm start
```

The app will open at `http://localhost:3000`

### Build for Production

```bash
npm run build
```

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React 18 |
| Styling | Inline CSS (no dependencies) |
| State | React Hooks (useState, useEffect) |
| Translation (demo) | Simulated — plug in Google Translate / DeepL API |

## 📱 Screens

| Screen | Description |
|--------|-------------|
| Home / Dial Pad | Country selector + number input + dial buttons |
| Active Call | Live translation feed + call controls |
| Contacts | Searchable contact list with flags |
| Recent Calls | Call history with type indicators |

## 🔌 Integrating Real Translation API

In `src/App.jsx`, replace the `TRANS` mock array with a real API call:

```js
// Example: Google Cloud Translation API
const translateText = async (text, targetLang) => {
  const res = await fetch(`https://translation.googleapis.com/language/translate/v2?key=YOUR_API_KEY`, {
    method: "POST",
    body: JSON.stringify({ q: text, target: targetLang }),
  });
  const data = await res.json();
  return data.data.translations[0].translatedText;
};
```

## 📄 License

MIT License — Free to use and modify.

## 👨‍💻 Author

Built with ❤️ for D Lingo Project
