# ✨ Our Little World ✨

> A cozy, single-page friendship website — no backend, no server, just vibes 🌸

---

## 💖 What Is This?

**Our Little World** is a self-contained friendship website built as a single HTML file. Everything runs in the browser — no servers, no databases, no accounts. It's a cozy digital scrapbook you can open, share, or host anywhere.

---

## 🌷 Features

### 🎵 Music Player
- Plays a default song on load
- Play / pause and volume controls
- **Upload your own MP3** directly from your device — the file never leaves your browser

### 💖 Click the Hearts Game
- Floating emoji hearts drift up the screen
- Click them to score points (+1 per heart)
- Touch-screen friendly
- Animated "+1 💕" feedback on every hit

### 📅 Feed the Days Calendar
- Displays the current month as a grid
- Toggle each day's heart between 🤍 (unfed) and 💖 (fed)
- Status **persists across page reloads** via `localStorage`
- Live summary: "You've fed ___ days this month 🌸"
- 🎊 **Confetti explosion** when every day in the month is fed!

### 💌 Letter Wall
- Write messages up to 200 characters
- Letters are **saved to `localStorage`** with date and time
- All posted letters appear as cute speech-bubble cards, newest first
- No delete needed — it's a keepsake wall

### 🐻 Bouncing Mascot
- A little bear sits in the corner and waves every time you:
  - Click a heart in the game
  - Toggle a calendar day
  - Post a letter

---

## 🚀 Getting Started

No installation, no dependencies, no build step.

1. **Download** `friendship.html`
2. **Open it** in any modern browser (Chrome, Firefox, Safari, Edge)
3. That's it 🎉

```bash
# Or clone this repo and open the file
git clone https://github.com/your-username/our-little-world.git
cd our-little-world
open friendship.html
```

---

## 🌐 Hosting

Because it's a single HTML file, you can host it anywhere static files are served:

| Platform | How |
|----------|-----|
| **GitHub Pages** | Push to a repo → Settings → Pages → Deploy from branch |
| **Netlify Drop** | Drag `friendship.html` to [netlify.com/drop](https://app.netlify.com/drop) |
| **Vercel** | `vercel --prod` in the project folder |
| **Any web server** | Just serve the file statically |

---

## 🗂️ Project Structure

```
our-little-world/
└── friendship.html   ← the entire app, everything inline
```

All CSS and JavaScript are embedded directly in the HTML file — no build tools, no bundlers, no `node_modules`.

---

## 🛠️ Tech Stack

- **HTML / CSS / JavaScript** — vanilla, no frameworks
- **Google Fonts** — [Caveat](https://fonts.google.com/specimen/Caveat) + [Nunito](https://fonts.google.com/specimen/Nunito) (loaded from CDN)
- **Canvas API** — for the floating hearts game
- **localStorage** — for calendar state and letter wall persistence
- **Web Audio API** — via native `<audio>` element + `URL.createObjectURL` for local file upload

---

## 📦 localStorage Keys

| Key | Value | Description |
|-----|-------|-------------|
| `cal_YYYY_M_D` | `"0"` or `"1"` | Fed status for each calendar day |
| `letters` | JSON array | All posted letters with text, date, and time |

Data is stored locally in the user's browser. Clearing browser storage will reset it.

---

## ✏️ Customisation

Everything lives in one file, so it's easy to tweak:

- **Default song** — change the `src` on the `<audio>` tag near the top of the `<script>` section
- **Mascot emoji** — find `🐻` in the HTML and swap it for any emoji
- **Colour palette** — all colours are CSS variables at the top of the `<style>` block:

```css
:root {
  --cream: #fff8f0;
  --blush: #fde8e8;
  --rose:  #f9c5c5;
  --accent: #e87070;
  /* ... */
}
```

- **Heart count** — change `NUM_HEARTS` in the script to control how many hearts float in the game

---

## 🌸 Browser Support

Works in all modern browsers that support:
- ES6 JavaScript
- Canvas API
- localStorage
- `URL.createObjectURL`

| Browser | Status |
|---------|--------|
| Chrome 80+ | ✅ |
| Firefox 75+ | ✅ |
| Safari 14+ | ✅ |
| Edge 80+ | ✅ |

---

## 📄 License

Do whatever you want with it 💕 Share it, modify it, make it yours.

---

<p align="center">made with 💖 · stay cozy always ✨</p>
