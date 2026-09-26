# Freehold Regional High School District School Planner

A school planner for Freehold Regional High School District students. The app is a single file that runs in the browser and can be deployed with GitHub Pages. Data is saved on the device; signing in also enables cloud sync.

## Features

- **Device-local storage** — everything saves to your browser's localStorage. Each laptop/phone keeps its own data. Works offline after first load.
- **Freehold Regional High School District 7-Day Rotating Block Schedule** — auto-calculates Day 1–7 for every school day. Click any Day badge to manually correct it if needed (e.g. after a holiday).
- **Flexible calendar views** — choose a Sunday–Saturday week, a rolling seven-day view centered on today, or a rolling seven-day view starting today. Your selected view is saved. Navigate by week or day, depending on the selected view.
- **Per-class task lists** — tap a class card to expand it, then add/check off/delete homework tasks.
- **Double labs** — configure a class as a double lab on up to two available letter days. The lab occupies consecutive schedule blocks, displays the correct continuation time for the selected school schedule, and saves with your class settings.
- **Focus timer** — use a countdown timer, stopwatch, or alarm at a selected time.
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

Planner settings and schedule data are saved in browser `localStorage` under `frhsd_v5` (with a separate key for each signed-in account).

- Guest data stays in that browser on that device. Clearing site data or switching browsers removes access to it.
- Signing in enables cloud sync between devices. Keep using the same account to access its synced data.
- Back up local data in browser DevTools under Application → Local Storage by copying the `frhsd_v5` value for the active user.

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
