# 🚀 BODMAS Mission — Interactive Math Learning Game

> **Assignment Submission** · Saurabh's EdTech Internship · March 2026  
> Built with: **HTML · CSS · JavaScript** (single-file, zero dependencies)

---

## 📸 Preview

```
┌──────────────────────────────────────────────────┐
│  ⬡ BODMAS MISSION          Score  Progress  🔥   │  ← Sticky HUD
├──────────────────────────────────────────────────┤
│  🔵 Brackets → ⭐ Orders → ➗÷ ✖️ → ➕ ➖        │  ← Priority bar
├──────────────────────────────────────────────────┤
│                                                  │
│         2  ×  ( 3  +  4 )  −  3²               │  ← Live equation
│                                                  │
│  🚌 Pipeline:  [🔵B]──[⭐O]──[✖️M]──[➖S]       │  ← Bus-Jam visual
│                                                  │
│   [ 5 ]   [ 23 ]   [ 19 ]   [ 7 ]              │  ← Answer zone
│                                                  │
│  💡 Hint          [ Check ✓ ]   [ Next › ]      │
├──────────────────────────────────────────────────┤
│  📡 Step-by-Step Solution (reveals after answer) │
└──────────────────────────────────────────────────┘
```

---

## 🎯 What This Game Teaches

**BODMAS** is the rule for the correct order of mathematical operations:

| Letter | Operation | Priority | Example |
|--------|-----------|----------|---------|
| **B** | **B**rackets | ① First | `(3 + 4)` → solve inside first |
| **O** | **O**rders (Powers/Roots) | ② Second | `3²` → calculate before +/− |
| **D** | **D**ivision | ③ Third | `12 ÷ 4` → left to right with × |
| **M** | **M**ultiplication | ③ Third | `3 × 5` → same level as ÷ |
| **A** | **A**ddition | ④ Fourth | `6 + 2` → left to right with − |
| **S** | **S**ubtraction | ④ Fourth | `9 − 3` → same level as + |

---

## 🗂 Project Structure

```
BODMAS_Mission/
│
├── index.html        ← The complete game (HTML + CSS + JS, all-in-one)
└── README.md         ← This file
```

> **Why a single file?**  
> The assignment specifies HTML + JS. Keeping everything in one file means  
> zero setup — open in any browser, works instantly, easy to host anywhere.

---

## 🚀 How to Run

### Option 1 — Open Directly (Quickest)
```
Double-click  index.html  in any file manager
```
Opens in your default browser. No server needed.

### Option 2 — Local Server (Recommended for sharing)
```bash
# Python 3
cd BODMAS_Mission
python -m http.server 8080
# Visit: http://localhost:8080
```

```bash
# Node.js (npx)
npx serve .
```

### Option 3 — Deploy Online (Free, instant link)
Upload `index.html` to any of:
- **[Netlify Drop](https://app.netlify.com/drop)** — drag & drop, get a live URL in 10 seconds
- **GitHub Pages** — push to repo → Settings → Pages → Deploy
- **Vercel** — `npx vercel` in the folder

---

## 🎮 Game Features

### 3 Question Types

| Type | Description | BODMAS Skill Practiced |
|------|-------------|----------------------|
| **Multiple Choice** | Tap the correct answer from 4 options | Computing final result |
| **Fill in the Blank** | Type the numeric answer | Precise step-by-step solving |
| **Drag to Reorder** | Drag operation steps into correct sequence | Understanding priority order |

### 3 Difficulty Levels

| Level | Concepts Covered | Example |
|-------|-----------------|---------|
| **Level 1** | Basic × before +, brackets, left-to-right | `2 + 3 × 4 = 14` |
| **Level 2** | Orders (powers), mixed operations | `3 + 4² − 2 = 17` |
| **Level 3** | Full BODMAS chains, nested operations | `(10 − 2²) × 3 + 1 = 19` |

### 🚌 Operation Pipeline (Bus-Jam Inspired Visual)
Every question shows a horizontal pipeline of "stations" — one for each operation needed to solve the equation. As the student answers, each station **lights up in sequence**, showing exactly which BODMAS rule fires at that step. Completed stations dim; the active one pulses. This directly mirrors the Bus-Jam game mechanic of sequential stops.

### Scoring System
```
Base points  = 100 × Level number
Streak bonus = +10 per consecutive correct answer
Hint penalty = 40% deduction (60 × Level instead of 100 × Level)
```

### Other Mechanics
- ❤️ **3 Lives** — game ends early if all lost
- 🔥 **Streak tracker** — consecutive correct answers
- 💡 **Hint system** — reveals first pipeline step, reduces score
- 📡 **Step-by-step explanation** — always shown after answering
- 🏆 **Results screen** — Score, Accuracy, Best Streak, Star rating

---

## 🎨 Design Decisions

### Visual Theme — Deep Space Mission
Each BODMAS letter is mapped to a glowing planet with a unique color:

| Operation | Color | Reason |
|-----------|-------|--------|
| Brackets | Cyan `#00D4FF` | Cool, first — like the North Star guiding you |
| Orders | Gold `#FFD700` | Power and energy — the sun |
| Division | Mint `#00FF88` | Clean, precise |
| Multiply | Orange `#FF6B35` | Warm, expansion |
| Addition | Violet `#A855F7` | Accumulation, growth |
| Subtraction | Rose `#FF3D71` | Reduction, loss |

### Why This Works Pedagogically
1. **Color coding** — each operation always appears in its designated color throughout the UI, building visual-spatial memory
2. **Pipeline animation** — students see the *sequence* of operations, not just the final answer
3. **Immediate feedback** — correct/wrong shown instantly with explanation
4. **Spaced variation** — 3 question types prevent rote clicking; students must understand, not guess
5. **Progressive difficulty** — confidence built at Level 1 before complexity of Level 3

---

## 🛠 Technical Notes

### Technologies Used
| Technology | Usage |
|------------|-------|
| **HTML5** | Structure, semantic markup |
| **CSS3** | Animations, glassmorphism, CSS variables, responsive grid |
| **Vanilla JavaScript** | Game engine, drag-and-drop, DOM manipulation |
| **Canvas API** | Animated starfield background |
| **Google Fonts** | Orbitron (display) + Exo 2 (body) — loaded via CDN |

### Browser Support
| Browser | Support |
|---------|---------|
| Chrome 90+ | ✅ Full |
| Firefox 88+ | ✅ Full |
| Safari 14+ | ✅ Full |
| Edge 90+ | ✅ Full |
| Mobile (iOS/Android) | ✅ Responsive |

### Performance
- Single HTTP request (excluding Google Fonts CDN)
- No build step, no npm install, no framework
- Canvas starfield uses `requestAnimationFrame` — GPU-accelerated
- All animations use CSS transforms (compositor thread — no layout thrash)

### Adding PHP Backend (Future Extension)
The game currently stores state in memory. To add persistent leaderboards or question banks via PHP:

```php
// scores.php — save score
<?php
header('Content-Type: application/json');
$data = json_decode(file_get_contents('php://input'), true);
// Insert into DB: $data['name'], $data['score'], $data['accuracy']
echo json_encode(['status' => 'saved']);
?>
```

```javascript
// In index.html — call after game ends
fetch('scores.php', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ name: 'Cadet', score: S.score, accuracy: pct })
});
```

---

## 📋 Question Bank Summary

| Q# | Level | Type | Expression | Answer |
|----|-------|------|------------|--------|
| 1 | 1 | MCQ | `2 + 3 × 4` | 14 |
| 2 | 1 | Fill | `(3 + 7) ÷ 2` | 5 |
| 3 | 1 | Sort | `8 − 2 + 5` | 11 |
| 4 | 2 | MCQ | `3 + 4² − 2` | 17 |
| 5 | 2 | Fill | `(5 + 3) × 2 − 4` | 12 |
| 6 | 2 | Sort | `12 ÷ 4 × 3` | 9 |
| 7 | 3 | MCQ | `2 × (3 + 4) − 3²` | 5 |
| 8 | 3 | Fill | `(10 − 2²) × 3 + 1` | 19 |
| 9 | 3 | Sort | `5 + 2 × 3 − 4 ÷ 2` | 9 |
| 10 | 3 | MCQ | `(6 + 2)² ÷ 4 − 1` | 15 |

Questions are **shuffled** on every playthrough so students can't memorise order.

---

## 🔮 Possible Extensions

- [ ] **PHP leaderboard** — save top scores to a database, show a class ranking table
- [ ] **Teacher dashboard** — track which questions students get wrong most often
- [ ] **More question types** — "spot the mistake" (fix the wrong answer), timed mode
- [ ] **Audio** — sound effects on correct/wrong, background ambient music
- [ ] **Curriculum levels** — CBSE / ICSE / UK National Curriculum mapping
- [ ] **Multiplayer** — two students race to answer the same question
- [ ] **Fraction Division game** — second game in the series (as per brief)

---

## 👨‍💻 Author Notes

This project was built as part of an internship assignment to demonstrate:
- Ability to translate a maths concept into an engaging interactive experience
- Understanding of visual learning principles (color, animation, sequencing)
- Clean, maintainable code without relying on heavy frameworks
- Production-quality UI/UX design from scratch

The Bus-Jam mechanic inspiration was implemented as the **Operation Pipeline** — a horizontal chain of operation stations that light up in sequence, giving students a visual "journey" through the equation rather than just a static answer.

---

*Made with ❤️ and a lot of `requestAnimationFrame`*
