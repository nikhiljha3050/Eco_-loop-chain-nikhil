# 🔄 EcoLoop-Chain

**Smart Resource Allocation & Circular Economy Platform**

A React SPA connecting waste producers (households, industry suppliers) with industry buyers through AI-powered waste scanning, certification, and auto-matchmaking.

![EcoLoop-Chain](https://img.shields.io/badge/React-19-61dafb?logo=react) ![Tailwind](https://img.shields.io/badge/Tailwind_CSS-v4-38bdf8?logo=tailwindcss) ![Vite](https://img.shields.io/badge/Vite-8-646CFF?logo=vite)

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🔀 **Role Switcher** | Toggle between Household Scrapper, Industry Supplier, and Industry Buyer |
| 📊 **Dashboard** | Real-time stats, activity feed, network health, environmental impact |
| 🎯 **Bounty Board** | Industry buyers post demand bounties (material type, grade, target price) |
| 📷 **AI Scanner** | Live webcam → Gemini Vision API → Batch Certificate with QR code |
| 🏪 **Marketplace** | Certified waste listings with search, QR codes, and certificate modals |
| ⚡ **Auto-Matchmaking** | `useEffect` compares listing tags vs bounty keywords → "Match Found!" alerts |

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Start dev server
npm run dev
# → http://localhost:5173/
```

## 🔑 Gemini Vision API

To enable real AI waste scanning, add your API key in `src/pages/AIScanner.jsx`:

```js
const GEMINI_API_KEY = "YOUR_GEMINI_API_KEY";
```

Without a key, the scanner returns randomized mock certificates.

## 🛠 Tech Stack

- **React 19** + **Vite 8** — fast SPA framework
- **Tailwind CSS v4** — dark industrial theme
- **react-webcam** — live camera feed
- **qrcode.react** — QR code generation
- **lucide-react** — icon library
- **react-router-dom** — client-side routing

## 📁 Project Structure

```
src/
├── context/
│   └── AppContext.jsx      # Global state, mock data, actions
├── components/
│   └── Navbar.jsx          # Top nav + role switcher
├── pages/
│   ├── Dashboard.jsx       # Command center
│   ├── BountyBoard.jsx     # Demand / bounty posting
│   ├── AIScanner.jsx       # Webcam + Gemini API + certificate
│   └── Marketplace.jsx     # Listings + modal + matchmaking
├── App.jsx                 # Router + layout
├── main.jsx                # Entry point
└── index.css               # Tailwind theme config
```

## 📄 License

MIT
