# ⚡ HABIT HERO

### Level up your life. One streak at a time. 🚀

**Habit Hero** is a modern, gamified habit-tracking web app that turns everyday routines into quests.

Complete habits → earn XP → build streaks → level up → become a legend. 🏆

<p align="center">
  <strong>🎮 Gamify your habits. 📈 Track your progress. 🔥 Build unstoppable streaks.</strong>
</p>

---

## ✨ Features

### 🎯 Gamified Habit Tracking

Turn your daily habits into quests and earn **+25 XP** every time you complete one.

### 🆙 XP & Level Progression

Your progress is represented through an RPG-style leveling system:

| Level | Hero Evolution |
| ----: | -------------- |
|     1 | 🥚 Egg         |
|     2 | 🐣 Hatchling   |
|     3 | 🦊 Apprentice  |
|     4 | 🦁 Warrior     |
|     5 | 🦄 Knight      |
|     6 | 🐉 Champion    |
|     7 | 👑 Legend      |
|     8 | 🌟 Mythic      |
|     9 | ⚡ Titan        |
|    10 | 🔱 Immortal    |

The app currently defines **10 progression levels**, with XP requirements scaling from 100 XP to 13,000 XP.

### 🔥 Habit Streaks

Every completed quest contributes to your streak, encouraging consistency and long-term habit building.

### 🏆 Global Leaderboard

Compete against other heroes and see your position based on XP.

The demo includes leaderboard characters such as **DragonSlayer, MorningStar, IronWill, ZenMaster, and NightOwl**.

### ➕ Create Custom Quests

Don't see your habit?

Create your own quest instantly with randomized icons and gradient themes.

### 🎉 Level-Up Experience

Reaching a new level triggers a dedicated celebration modal with:

* 🎊 Level-up animation
* ✨ New hero evolution
* 🎆 Confetti effects
* ⚔️ Continue Quest interaction

### 💥 Interactive Animations

Habit Hero includes a variety of micro-interactions and animations:

* Floating UI elements
* Glowing cards
* Animated progress bars
* Button interactions
* Slide-up habit cards
* Pulse effects
* Level-up transitions
* Custom canvas confetti

The interface uses custom CSS animations alongside Tailwind CSS for the visual effects.

### 📅 Date Navigation

Navigate between dates and review your quests from previous days.

### 🔔 Toast Notifications

Get instant feedback when completing or creating quests.

### ⌨️ Keyboard Support

Press **Escape** to close active modals.

---

## 🎨 UI & Design

Habit Hero uses a dark, futuristic aesthetic inspired by modern gaming dashboards.

### Design highlights

* 🌌 Dark slate background
* 💜 Purple / cyan / pink gradients
* 🪟 Glassmorphism panels
* ✨ Soft glow effects
* 🎮 RPG-inspired progression
* 📱 Responsive layout
* 🧊 Rounded modern components
* ⚡ Smooth micro-interactions

The UI uses **Inter** as its primary typeface and Tailwind CSS via CDN.

---

## 🛠️ Tech Stack

| Technology             | Purpose                   |
| ---------------------- | ------------------------- |
| **HTML5**              | Application structure     |
| **Tailwind CSS**       | Styling & responsive UI   |
| **Vanilla JavaScript** | Application logic & state |
| **CSS Animations**     | UI motion & transitions   |
| **HTML Canvas**        | Confetti particle system  |
| **Google Fonts**       | Inter typography          |

No framework.
No build step.
No backend.
Just open the HTML file and play. ⚡

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/habit-hero.git
```

### 2. Enter the project

```bash
cd habit-hero
```

### 3. Launch the app

Because Habit Hero is a standalone HTML application, you can simply open:

```text
index.html
```

in your browser.

For the best development experience, use a local development server such as VS Code Live Server.

---

## 📂 Project Structure

```text
habit-hero/
│
├── index.html
└── README.md
```

The current implementation keeps the entire application—including markup, styling, state management, rendering, interactions, and confetti engine—in a single HTML file.

---

## 🧠 How It Works

Habit Hero maintains an in-memory application state containing:

```js
{
  xp: 0,
  level: 1,
  streak: 0,
  completedToday: 0,
  currentDateOffset: 0,
  habits: [],
  leaderboard: []
}
```

When a habit is completed:

```text
Complete Quest
      ↓
   +25 XP
      ↓
 Increase Streak
      ↓
 Update Statistics
      ↓
 Check Level
      ↓
 Level Up? ── Yes ──→ 🎉 Celebration
      │
      No
      ↓
   Re-render UI
```

The core completion flow increments XP, updates streak information, checks the next level threshold, triggers confetti, displays a toast, and re-renders the application.

---

## 🎮 Core Gameplay Loop

### 01 — Create a Quest

Add a habit such as:

```text
💧 Drink 8 glasses of water
🏃 30 min exercise
📖 Read 20 pages
🧘 10 min meditation
🥗 Eat a healthy meal
```

### 02 — Complete It

Click the quest button to mark the habit as complete.

### 03 — Earn XP

Every completed habit awards:

```text
+25 XP
```

### 04 — Build Your Streak

Consistently complete habits and watch your streak grow.

### 05 — Evolve

Earn enough XP to unlock the next hero form.

### 06 — Climb the Leaderboard

Your ranking is calculated against the available leaderboard players based on XP.

---

## 🌟 Current Demo Habits

The initial experience ships with five example quests:

* 💧 Drink 8 glasses of water
* 🏃 30 min exercise
* 📖 Read 20 pages
* 🧘 10 min meditation
* 🥗 Eat a healthy meal

Each habit has its own gradient, icon, and starting streak.

---

## 🔮 Roadmap

Habit Hero currently focuses on the front-end gamification experience.

Potential future upgrades:

* [ ] 💾 Persistent data with LocalStorage
* [ ] 👤 User accounts & authentication
* [ ] ☁️ Cloud synchronization
* [ ] 📊 Habit analytics dashboard
* [ ] 📈 Weekly & monthly statistics
* [ ] 🏅 Achievement system
* [ ] 🎁 Daily rewards
* [ ] 🔥 Streak protection
* [ ] 👥 Real multiplayer leaderboard
* [ ] 🤝 Team challenges
* [ ] 📱 PWA / mobile installation
* [ ] 🌙 Custom themes
* [ ] 🔔 Notifications & reminders
* [ ] 🗄️ Backend database

> **Team Challenges** are already teased in the interface as a future feature.

---

## ⚠️ Current Limitations

This project is currently a **front-end prototype/demo**.

### Data persistence

Application state is stored in JavaScript memory, so refreshing the page resets progress.

### Leaderboard

The leaderboard is currently populated with static demo data rather than a real backend.

### Historical dates

Past-date habit completion is currently simulated rather than persisted.

### Authentication

There is currently no user authentication or account system.

These limitations make the project especially suitable as a foundation for adding a backend and persistent data layer.

---

## 🧩 Customization

You can easily customize the experience by modifying:

### Habits

Edit the initial `habits` array:

```js
habits: [
  {
    id: 1,
    name: "💧 Drink 8 glasses of water",
    completed: false,
    streak: 5,
    color: "from-cyan-500 to-blue-600",
    icon: "💧"
  }
]
```

### Level System

Modify the `LEVELS` array to create your own progression system:

```js
const LEVELS = [
  { level: 1, name: "Egg", emoji: "🥚", xpNeeded: 100 },
  { level: 2, name: "Hatchling", emoji: "🐣", xpNeeded: 250 },
  // ...
];
```

### XP Rewards

Change the XP reward inside `toggleHabit()`:

```js
state.xp += 25;
```

Want harder quests?

```js
state.xp += 50;
```

Want a slower progression system?

Increase the XP thresholds in `LEVELS`.

---

## 💡 Why Habit Hero?

Most habit trackers focus on lists and checkboxes.

Habit Hero focuses on **motivation**.

Instead of:

> "I completed my habit."

You get:

> **QUEST COMPLETE! 🎉 +25 XP**

Instead of:

> "I've been consistent."

You get:

> **🔥 STREAK +1**

Instead of:

> "I've reached another milestone."

You get:

> **⚔️ LEVEL UP!**

The goal is simple:

### Make consistency feel rewarding.

---

## 🤝 Contributing

Contributions are welcome!

If you'd like to improve Habit Hero:

1. Fork the repository
2. Create a feature branch

```bash
git checkout -b feature/amazing-feature
```

3. Commit your changes

```bash
git commit -m "feat: add amazing feature"
```

4. Push your branch

```bash
git push origin feature/amazing-feature
```

5. Open a Pull Request 🚀

---

## 📜 License

This project is open source and available under the **MIT License**.

---

## ⭐ Support

If you enjoyed Habit Hero:

⭐ **Star the repository**

🍴 **Fork the project**

🐛 **Open an issue**

💡 **Suggest a feature**

And most importantly...

### Keep your streak alive. 🔥

---

<p align="center">

**HABIT HERO**
*Level up your life. One streak at a time.*

⚡ Built with HTML · Tailwind CSS · JavaScript · Canvas

</p>
