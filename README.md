# 🎮 Student Mental Health Simulator

> A text-based, turn-based life simulation game written in C.
> Navigate a brutal 5-day academic week — every choice has real consequences.

![Language](https://img.shields.io/badge/Language-C-blue)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20Mac-lightgrey)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Course](https://img.shields.io/badge/Course-CSE10010-orange)

---

## 📖 About

The **Student Mental Health Simulator** puts you in the shoes of a student grinding through a 5-day academic week. Each day you make ONE decision — study, scroll reels, game, sleep, or hang out. Every choice shifts your stats: Energy, Happiness, Stress, and Productivity.

Make bad decisions long enough and you burned out. Make smart ones and you might just pull off an A.

Built entirely in **C** with no external libraries — just standard I/O, file handling, and game logic.

---

## 🚀 Getting Started

### Prerequisites
- GCC compiler installed
- Terminal / Command Prompt

### Compile & Run

**Windows:**
```bash
gcc main.c -o game
game
```

**Linux / Mac:**
```bash
gcc main.c -o game
./game
```

> ⚠️ Keep the filename simple — no spaces. Use `main.c`, not `student mental simulation.c`.

---

## 🎮 Gameplay

### Actions Available Each Day

| # | Action | Productivity | Energy | Happiness | Stress |
|---|---|---|---|---|---|
| 1 | 📚 Study | +20 | -20 | -5 | +10 |
| 2 | 📱 Reels | 0 | -10 | +8 | -5 |
| 3 | 🎮 Game | 0 | -15 | +15 | -10 |
| 4 | 😴 Sleep | -5 | +30 | 0 | -8 |
| 5 | 🤝 Hangout | -8 | -20 | +20 | +5 |

> Stats scale with day — deadlines increase stress penalties and productivity bonuses as the week progresses.

### Day Themes

| Day | Theme | Effect |
|---|---|---|
| 1 | Monday Blues | No modifiers |
| 2 | Tuesday Tension | Study costs +5 stress |
| 3 | Midweek Crisis | Study costs +5 stress |
| 4 | Panic Rising | Study gives +5 productivity, +10 stress |
| 5 | DEADLINE PANIC! | Study gives +10 productivity, +15 stress |

---

## ⚙️ Features

- 💾 **Save / Load System** — progress saved to `student_data.txt` automatically
- 🔐 **Player Authentication** — save file locked to your name
- ⏱️ **Two Game Modes** — Speedrun (no wait) or Realism (24h cooldown between days)
- 🎲 **Random Events** — 33% chance of a surprise event each day
- 🔥 **Study Streak Bonus** — study two days in a row for +10 productivity
- 💔 **Low Happiness Penalty** — studying at 0 happiness halves your productivity gain
- 😵 **Burnout & Exhaustion** — hitting stress 100 or energy 0 forces a rest turn
- 📊 **Final Report Card** — grade, regret score, and a player identity label

---

## 🏆 Grading

| Grade | Avg Productivity |
|---|---|
| A | ≥ 90 |
| B | ≥ 75 |
| C | ≥ 55 |
| D | ≥ 35 |
| F | < 35 |

**Regret Score Formula:**
```
Regret = (100 - avg_productivity) + stress - (happiness / 2)
```
Lower is better. Zero regret = perfect run.

---

## 🪪 Player Identities

| Identity | Condition |
|---|---|
| 🔫 Academic Weapon | Avg ≥ 80, stress under control |
| 🔥 Burnt Out | Avg ≥ 80 but stress > 60 |
| 🤫 Quiet Grinder | Grade A or B |
| 😄 Happy-Go-Lucky | Happiness > 70 but avg < 40 |
| 😰 Eternal Slacker in Panic | Stress > 70 and avg < 50 |
| 😱 Panic Master | Regret score ≥ 70 |
| 😤 Survivor | Everything else |

---

## 🗂️ Project Structure

```
📁 Student-Mental-Health-Simulator/
├── main.c               ← Full game source code
├── student_data.txt     ← Auto-generated save file (gitignored)
└── README.md            ← You are here
```

---

## 🛠️ Built With

- **Language:** C (C99)
- **Compiler:** GCC
- **IDE:** Visual Studio Code
- **Version Control:** Git / GitHub

---

## 📄 License

This project was built for academic purposes as part of CSE10010 at MIT-WPU, Pune.
Feel free to fork, learn from it, or improve it.

---

<p align="center">Made with ☕ and deadline panic by Team MIT-WPU CSE 2025-26</p>
