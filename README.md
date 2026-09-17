# Freehold Regional High School District School Planner

An AI-powered weekly school planner for Freehold Regional High School District students. Single-file, runs entirely in the browser via GitHub Pages. **Each device saves its own data** — no accounts, no server, no sign-in.

## Features

- **Device-local storage** — everything saves to your browser's localStorage. Each laptop/phone keeps its own data. Works offline after first load.
- **Freehold Regional High School District 7-Day Rotating Block Schedule** — auto-calculates Day 1–7 for every school day. Click any Day badge to manually correct it if needed (e.g. after a holiday).
- **Weekly view** — Google Tasks-style Sun–Sat columns. Navigate any week past or future with the arrow buttons.
- **Per-class task lists** — tap a class card to expand it, then add/check off/delete homework tasks.
- **Weekend reminder cards** — free-day cards on Saturday and Sunday for general reminders.
- **Day number override** — click any **Day X** badge in the week header to manually set that day's block number. The rest of the week recalculates from your choice. A ✎ shows when overridden; tap "Auto" to revert.
- **SVG logo** — book icon with a rotating day badge.
- **No sign-in required** — just open the URL and go.

---

## Setup

### 1. Deploy to GitHub Pages

1. Fork or push this repo to your GitHub account
2. Go to **Settings → Pages**
3. Set Source: **main** branch, **/ (root)**
4. Visit `https://yourusername.github.io/frhsd-planner/`
5. Set your school type and enter your periods on first launch — done!

---

## How data is stored

All data lives in **`localStorage`** in your browser under the key `frhsd_planner_v3`.

- If you clear your browser's site data or use a different browser, your data will be gone.
- Different laptops/devices each start fresh with their own data.
- There is no sync between devices — this is by design.

To back up your data: open browser DevTools → Application → Local Storage → copy the value.

---

## Block Schedule Reference

Freehold Regional High School District uses a **7-day rotating block** schedule. Each school day is labeled Day 1–7 (not by weekday). Each day has 5 blocks. Your subjects rotate through the blocks each day.

| Day | B1     | B2     | B3     | B4     | B5     |
|-----|--------|--------|--------|--------|--------|
| 1   | Subj 1 | Subj 2 | Subj 3 | Subj 4 | Subj 5 |
| 2   | Subj 2 | Subj 3 | Subj 4 | Subj 5 | Subj 1 |
| 3   | Subj 3 | Subj 4 | Subj 5 | Subj 1 | Subj 2 |
| ... | ...    | ...    | ...    | ...    | ...    |

Anchor: **Sep 9, 2025 = Day 1** (first student day of 2025–2026 school year).

Bell schedule (Early schools — Freehold, Howell, Manalapan):
- Block 1: 7:30–8:37 AM
- Block 2: 8:42–9:49 AM
- Block 3: 9:54–11:01 AM
- Block 4: 11:47 AM–12:54 PM
- Block 5: 12:59–2:06 PM

Bell schedule (Late schools — Colts Neck, Freehold Township, Marlboro):
- Block 1: 8:24–9:31 AM
- Block 2: 9:36–10:43 AM
- Block 3: 10:48–11:55 AM
- Block 4: 12:41–1:48 PM
- Block 5: 1:53–3:00 PM

---

## File Structure

```
Freehold Regional High School District-planner/
├── index.html      # The entire app — HTML + CSS + JS, single file, no dependencies
├── .env.example    # Reference only — Supabase keys are stored in the app configuration
└── README.md
```
