# Studle

## A new way to study. Made by students.

Studle is a web-based flashcard and study-set application built with React. Sign in with Google, create hierarchical study sets, quiz yourself in multiple choice or written mode, share sets with others, and collect cosmetic stickers.

**Authors:** Ilan Bernstein and Liam Bridgers

---

## Features

### Study Sets
- **Create sets** with a three-step wizard: define topics (with nesting), add facts (question/answer pairs), and optionally provide extra wrong answers for multiple-choice mode.
- **Edit existing sets** at any time.
- **Study mode** supports two question styles:
  - **Multiple Choice** — select the correct answer from generated options.
  - **Written** — type the answer from memory.
- Choose which topics to include before each session.
- **Session summary** with score breakdown; perfect scores trigger a confetti animation.

### Sharing
- Every set has a shareable **Studle ID** (6 letters).
- Anyone with the ID can **Study Now** (temporary, no account required) or **Copy & Save** the set to their own account.

### Sticker Market
- Earn **tickets** through studying and spend them in the Market.
- Stickers come in tiers: Common, Uncommon, Rare, Legendary, and Special.
- Owned stickers can be placed anywhere on the Home page and dragged to reposition.

### Settings
- **Dark Mode** — toggle a dark color scheme.
- **Show Confetti** — enable/disable the confetti animation on perfect scores.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | React 18 + Vite |
| UI Library | Material UI (MUI v5) |
| Auth | Google OAuth (`@react-oauth/google`, `gapi-script`) |
| Real-time | Socket.IO client, `react-use-websocket` |
| Drag & Drop | `react-draggable` |
| Charts | Recharts |
| Backend | REST API (separate service) |

---

## Getting Started

### Prerequisites
- Node.js 16+
- npm

### Install & Run

```bash
npm install
npm run dev
```

The app will be available at `http://localhost:5173` by default.

### Other Scripts

```bash
npm run build    # Production build (outputs to dist/)
npm run preview  # Preview the production build locally
```

---

## Project Structure

```
src/
├── App.jsx                  # Root component, routing, sticker overlay
├── landingPage.jsx          # Sign-in screen
├── homePage.jsx             # Dashboard — recent sets, sticker library
├── loginManager.jsx         # Google OAuth logic
├── constants.js             # Backend URL
├── themes.js                # Light/dark MUI themes
├── Create_Set/              # Set creation wizard
│   ├── createSetPage.jsx
│   ├── createTopicsPage.jsx
│   ├── createFactsPage.jsx
│   └── createExtraAnswersPage.jsx
├── Study_Set/               # Study session flow
│   ├── studySetPage.jsx
│   ├── studySetOptions.jsx
│   ├── studySetQuestioner.jsx
│   └── studySetSummary.jsx
├── Market/                  # Sticker marketplace
│   ├── marketPage.jsx
│   └── stickerInfo.js
└── Settings/                # User preferences
    ├── settingsPage.jsx
    └── settings.jsx
```

---

## License

This project is licensed under the **GNU General Public License v3.0**. See [COPYING](COPYING) for details.

Copyright (C) 2023 Ilan Bernstein and Liam Bridgers
