# 🏏 IPL Auction — Live Fantasy Bidding Platform

A full-featured IPL fantasy auction app built with React + Vite.  
Host live auctions with friends, bid on real IPL 2025 players, and build your dream squad.

## 🚀 Live Demo
Once deployed: `https://<your-username>.github.io/ipl-auction/`

---

## 📁 Project Structure

```
ipl-auction/
├── .github/
│   └── workflows/
│       └── deploy.yml        ← Auto-deploy to GitHub Pages on push to main
├── src/
│   ├── main.jsx              ← React entry point
│   └── IPLAuction.jsx        ← Complete app (all screens + logic)
├── index.html                ← HTML shell
├── vite.config.js            ← Vite config (set your repo name here)
├── package.json              ← Dependencies + scripts
├── .gitignore
└── README.md
```

---

## ⚙️ Local Development

```bash
# 1. Install dependencies
npm install

# 2. Start dev server
npm run dev

# 3. Open http://localhost:5173
```

---

## 🌐 Deploy to GitHub Pages

### Option A — Automatic (recommended)
Every push to `main` auto-deploys via GitHub Actions.

1. Push this repo to GitHub
2. Go to **Settings → Pages → Source** → select **GitHub Actions**
3. That's it — your site deploys automatically on every push ✅

### Option B — Manual one-time deploy
```bash
npm install
npm run deploy
```
Then set **Settings → Pages → Source → Deploy from a branch → gh-pages**.

---

## ⚠️ One Required Edit

Open `vite.config.js` and change the `base` to match your GitHub repo name:

```js
base: '/YOUR-EXACT-REPO-NAME/',
```

Example: if your repo URL is `github.com/johndoe/ipl-auction`, set:
```js
base: '/ipl-auction/',
```

---

## 🏏 Features

- **60+ real IPL 2025 players** across 4 pools (Marquee → Emerging)
- **Live bidding** with 15-second countdown timer
- **Anti-snipe protection** — bid in last 3s resets timer to 8s
- **Smart validation** — purse limits, squad cap (25), overseas cap (8), role minimums
- **Bot opponents** with realistic bidding strategy
- **Sold/Unsold overlays** with dramatic animations
- **My Squad drawer** — live purse tracker + role breakdown
- **Auction log** — scrollable feed of every bid event
- **Results page** — full squads, unsold players, bid history

---

## 🛠 Tech Stack

| Layer | Tech |
|-------|------|
| UI Framework | React 18 |
| Build Tool | Vite 5 |
| Styling | Pure CSS-in-JS (inline styles) |
| State | useState + useReducer hooks |
| Real-time | setInterval (timer) + useCallback (bot AI) |
| Deploy | GitHub Pages via GitHub Actions |
