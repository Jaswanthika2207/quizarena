# QuizArena 🏆 — Epic Online Quiz Battle System

> A feature-rich, real-time quiz battle platform built with pure HTML, CSS & JavaScript.

---

## 🚀 How to Play

### Step 1 — Open `index.html`
Open `index.html` in your browser (Chrome/Edge recommended).

### Step 2 — Host Creates Room (Tab 1)
1. Click **"Host Game"** → fill in quiz title + your name
2. Add questions (MCQ or True/False with custom time limits)
3. Click **"Create Room & Open Lobby"**
4. Share the **6-character room code** with players

### Step 3 — Players Join (Each in a new Tab)
1. Open a new browser tab → navigate to **`join.html`**
2. Enter the **room code** from the host
3. Type your name & pick your **avatar + color**
4. Wait in the lobby

### Step 4 — Host Starts the Game
- Back in Tab 1 (host), click **"Start Game"** once players are in the lobby

### Step 5 — Answer & Battle!
- Questions appear with a countdown timer
- **Faster answers = MORE points** (up to 1000 pts/question)
- Use your **power-ups** wisely!

### Step 6 — View Results
- Final leaderboard with podium, scores & rankings

---

## ⚡ Power-Ups (Each usable ONCE per game)

| Power | Icon | Effect |
|-------|------|--------|
| **Time Freeze** | ❄️ | Freezes everyone's timer for 6 seconds |
| **Double Points** | ⚡ | Doubles your score for the current question |
| **50-50 Lifeline** | 🎯 | Removes 2 wrong answers from the choices |

---

## 🛡️ Anti-Cheat System
- **Tab switching** is detected → warning + -50 point penalty per switch
- **Window focus loss** is monitored
- Right-click & keyboard shortcuts (Ctrl+C, F12) are disabled
- All cheat events are reported to the host in real-time

---

## 📊 Scoring System
- Max **1000 points** per question (configurable: 500–2000)
- Score = `basePoints × (0.4 + 0.6 × timeLeft/maxTime)`
- **Speed bonus**: answering in the first 2 seconds gives near-max points
- **Streak bonus**: 3+ consecutive correct answers = +50 bonus points

---

## 🖥️ File Structure
```
online assessment web/
├── index.html       ← Landing page (Host/Join choice)
├── host.html        ← Host: create quiz, manage lobby
├── join.html        ← Players: join with avatar selection
├── game.html        ← Live game (host controls + player answers)
├── results.html     ← Final leaderboard + podium
├── css/
│   └── style.css    ← Full design system (dark glassmorphism)
└── js/
    └── app.js       ← Shared utilities, BroadcastChannel engine
```

---

## 🔧 Technical Notes
- Uses **BroadcastChannel API** for real-time tab-to-tab communication
- Works across **multiple tabs in the same browser** on one machine
- No backend, no server, no dependencies — **100% pure HTML/JS**
- Supports **MCQ** (4 options) and **True/False** question types
- Customizable time limits per question (10–60 seconds)

---

## 🎨 Features
- ✅ 24 custom emoji avatars + 8 gradient color themes
- ✅ Animated glassmorphism dark UI
- ✅ Live lobby with real-time player cards
- ✅ Circular countdown timer with color warnings (green → orange → red)
- ✅ Score popup animations on correct answers
- ✅ Confetti celebration for top 3 players
- ✅ Live leaderboard on host screen during game
- ✅ Podium animation on results page
- ✅ Streak tracking (3+ correct in a row = bonus!)
