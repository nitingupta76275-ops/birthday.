# A Little Birthday Story

A mobile-first, cinematic birthday surprise website built with React, Vite, GSAP, Framer Motion and Three.js. Your four supplied photographs are included locally in `src/assets/images/`; no photo is uploaded to a third-party service.

## Personalise it first

Open `src/config/siteConfig.js` and edit:

- `girlfriendName` — the name shown in the intro, hero and finale.
- `senderName` — the website credit.
- `birthdayDate` — birthday date in `YYYY-MM-DD` format.
- `pin` — the four-digit personal surprise code (default `2026`).
- `heroMessage`, `letter`, `surpriseNote`, `appreciations`, and `memories`.
- `photos` — replace imported images or add new images under `src/assets/images/`.

The PIN gate is a fun personal reveal only. It is not real authentication; the PIN is present in client-side source code.

## Add your own audio

Put an audio file in `src/assets/audio/`, then import it in `siteConfig.js` and set `music.audioFile` to that import. To show a voice note, set `voiceMessage` to an imported audio file path. The voice-message section stays hidden when that value is empty.

## Run locally

Requires Node.js 20.19+ or 22.12+.

```bash
npm install
npm run dev
```

Open the local URL printed by Vite.

## Production build

```bash
npm run build
npm run preview
```

The static production site is generated in `dist/`.

## Deploy to Vercel

Import this folder as a Vite project in Vercel. The default Vite settings work: build command `npm run build`, output directory `dist`. No environment variables or backend are required.

## Project structure

```text
birthday-surprise/
├── index.html
├── package.json
├── vite.config.js
├── README.md
├── .gitignore
└── src/
    ├── App.jsx
    ├── main.jsx
    ├── assets/
    │   ├── images/              # Four supplied personal photos
    │   └── audio/               # Add optional music / voice files here
    ├── config/siteConfig.js     # Main personalisation file
    ├── components/              # Reusable UI components can live here
    ├── data/                    # Extendable content data folder
    ├── sections/                # Extendable chapter sections
    ├── styles/global.css
    └── three/CakeScene.jsx      # Three.js cake and candle scene
```

## Included interactions

- Fast animated loader and four-digit PIN reveal.
- Cinematic intro and full-height photo hero.
- Scroll-revealed memory timeline and responsive photo gallery/lightbox.
- Appreciation stories, a three-step quiz, touch/mouse scratch card and gift reveal.
- Openable birthday letter, optional music and optional voice note.
- Three.js layered cake with candles, plus confetti celebration.
- Hidden star easter egg and replay controls.
- Reduced-motion support, keyboard-friendly native buttons, responsive layout and `noindex,nofollow` metadata.

## Privacy note

The photos stay in the local project unless you choose to deploy the website. Anyone with access to the deployed URL can view the page assets; the client-side PIN is not a privacy/security boundary. Share the deployed link thoughtfully.
