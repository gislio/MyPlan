# MyPlan — AI Life Planning & Coaching System

A comprehensive life planning and coaching plugin for [Claude](https://claude.ai) desktop app (Cowork mode). Built on research from **100+ books** and cutting-edge behavioral science, MyPlan helps you discover your purpose, design your life, set and achieve goals, build positive habits, manage your energy, stay motivated, and plan your days, weeks, months, and years.

MyPlan acts as your personal life coach — warm, encouraging, and grounded in science. It remembers your progress across sessions, adapts to your preferences, and grows with you over time.

---

## What's Inside

### 9 Specialist Coaching Agents

| Agent | What It Does |
|-------|-------------|
| **MyPlan** | Master orchestrator — onboards you, shows your dashboard, and routes you to the right specialist |
| **MyPlan-Purpose** | Guides purpose discovery using Ikigai, values clarification, Frankl's meaning pathways, and legacy visioning |
| **MyPlan-LifePlan** | Creates a comprehensive life plan across 10 life domains with multi-horizon visioning (1 to 25 years) |
| **MyPlan-Goals** | Sets and tracks goals using the 12 Week Year, 4 Disciplines of Execution, SMARTER goals, and RPM |
| **MyPlan-Habits** | Designs new habits and breaks bad ones using Atomic Habits, Tiny Habits, and behavioral science |
| **MyPlan-Daily** | Plans your days and weeks with time blocking, Big 3 priorities, and energy-based scheduling |
| **MyPlan-Energy** | Optimizes energy, sleep, exercise, and recovery using the Power of Full Engagement model |
| **MyPlan-Motivation** | Helps you get unstuck using Self-Determination Theory, WOOP, growth mindset, and procrastination science |
| **MyPlan-Review** | Conducts daily, weekly, monthly, quarterly, and annual reviews (quick report or guided conversation) |

### 3 Schedulable Commands

| Command | Purpose | Suggested Schedule |
|---------|---------|-------------------|
| `/daily-checkin` | Morning planning or evening review | Every day |
| `/weekly-review` | Reflect on the past week, plan the next | Every Sunday |
| `/monthly-review` | Deep progress check and course correction | 1st of each month |

### Persistent Memory via Markdown Files

All your progress is tracked in plain markdown files in `life-compass-data/`. The agents read and write these files to maintain continuity across sessions — they remember your values, goals, habits, energy patterns, and every coaching conversation.

| File | What It Tracks |
|------|---------------|
| `user_profile.md` | Your name, values, strengths, life domain ratings, chronotype, and coaching preferences |
| `journal.md` | A running log of every coaching session, review, decision, and milestone |
| `life_plan.md` | Your comprehensive life plan across 10 domains (health, career, relationships, etc.) |
| `goals.md` | Active goals with quarterly targets, lead measures, and progress tracking |
| `habits.md` | Habit tracker with streaks, stages (initiation → automatic), and weekly scorecards |
| `energy_log.md` | Energy, sleep, stress, and wellness tracking with pattern analysis |
| `daily_plan.md` | Current daily and weekly plans with time blocks and reflections |

---

## Installation

### Prerequisites

- **Claude desktop app** with Cowork mode enabled
- A folder on your computer where you'd like to store your life planning data

### Step 1: Install the Plugin

**Option A — Install from the `.plugin` file (easiest):**

1. Download the `myplan-plugin.plugin` file from the [Releases](../../releases) page (or build it yourself — see below)
2. Open Claude desktop app
3. Drag and drop the `.plugin` file into a Cowork session, or navigate to Settings → Plugins and install from file
4. The plugin will appear in your available skills

**Option B — Install manually from source:**

1. Clone or download this repository
2. Copy the `myplan-plugin/` folder to your Claude plugins directory:
   - **macOS**: `~/Documents/Claude/plugins/myplan-plugin/`
   - Or wherever your Claude desktop app stores plugins
3. Restart Claude desktop app — the MyPlan skills should appear

**Option C — Build the `.plugin` file from source:**

1. Clone this repository
2. Run:
   ```bash
   cd myplan-plugin
   zip -r ../myplan.plugin . -x "*.DS_Store"
   ```
3. Install the resulting `myplan.plugin` file using Option A

### Step 2: Set Up Your Data Folder

1. Copy the `life-compass-data/` folder from this repository into the project folder you'll use with Cowork mode
2. The folder contains empty template files — MyPlan will populate them during onboarding

Your project folder should look like this:
```
your-project-folder/
└── life-compass-data/
    ├── user_profile.md
    ├── journal.md
    ├── life_plan.md
    ├── goals.md
    ├── habits.md
    ├── energy_log.md
    └── daily_plan.md
```

### Step 3: Start Using MyPlan

1. Open Claude desktop app in Cowork mode
2. Select the folder containing your `life-compass-data/` directory
3. Type **"MyPlan"** or **"help me plan my life"**
4. The system will walk you through a conversational onboarding

---

## Setting Up Scheduled Check-ins

Once installed, you can set up automatic daily, weekly, and monthly check-ins:

1. In a Cowork session, type `/daily-checkin` to run your first daily check-in
2. To schedule it automatically, use the Schedule skill:
   - Say "Schedule my daily check-in for 8am every day"
   - Say "Schedule my weekly review for Sunday mornings"
   - Say "Schedule my monthly review for the 1st of each month"
3. Approve tool permissions on the first run so future automatic runs proceed without interruption

---

## How It Works

### The Coaching Approach

MyPlan uses a **Socratic coaching** style — it asks powerful questions before offering advice. Drawing from research in coaching psychology, it:

- Addresses you by name and remembers your context
- Asks clarifying questions before prescribing solutions
- Celebrates progress, no matter how small
- Connects every action back to your stated purpose and values
- Offers both quick check-ins and deep guided conversations

### The Planning Architecture

MyPlan implements a multi-horizon planning system:

```
Life Purpose & Values (foundation)
    ↓
Life Vision (25-year, 10-year, 5-year)
    ↓
Annual Goals & Theme
    ↓
Quarterly Goals (12-week sprints)
    ↓
Weekly Big Rocks
    ↓
Daily Big 3 Priorities
    ↓
Habits & Routines (the daily engine)
```

Each level connects to the ones above and below it, so your daily actions stay aligned with your deepest values.

### Two Operating Modes

For every check-in and review, you can choose:

- **Quick Report** — the agent reads your data, generates a progress summary, and asks 2-3 targeted questions
- **Guided Conversation** — the agent walks you through a reflective session step by step

Set your default preference during onboarding, or switch on any given day.

---

## Research Foundation

This system synthesizes frameworks from over 100 books, including:

**Goal Setting**: Locke & Latham (Goal Setting Theory), Brian Tracy (Goals!), Moran & Lennington (The 12 Week Year), McChesney, Covey & Huling (4 Disciplines of Execution)

**Habits & Behavior Change**: James Clear (Atomic Habits), BJ Fogg (Tiny Habits), Hal Elrod (The Miracle Morning), Gollwitzer (Implementation Intentions), COM-B Model

**Productivity & Time Management**: David Allen (Getting Things Done), Cal Newport (Deep Work, Slow Productivity), Stephen Covey (7 Habits, First Things First), Greg McKeown (Essentialism)

**Motivation & Mindset**: Daniel Pink (Drive), Carol Dweck (Mindset), Mihaly Csikszentmihalyi (Flow), Gabriele Oettingen (WOOP), Self-Determination Theory

**Life Design**: Bill Burnett & Dave Evans (Designing Your Life), Michael Hyatt (Living Forward, Your Best Year Ever), Tony Robbins (RPM System)

**Energy & Performance**: Jim Loehr & Tony Schwartz (The Power of Full Engagement), Chris Bailey (Hyperfocus), Ali Abdaal (Feel-Good Productivity)

**Purpose & Meaning**: Viktor Frankl (Man's Search for Meaning), Ikigai research, Martin Seligman (PERMA), Blue Zones longevity research

**Behavioral Science**: Nudge theory, Choice Architecture, Transtheoretical Model, Behavioral Activation, Coaching Psychology

---

## Repository Structure

```
github-share/
├── README.md                    ← You are here
├── myplan-plugin/               ← The installable plugin
│   ├── .claude-plugin/
│   │   └── plugin.json          ← Plugin manifest
│   ├── skills/                  ← 9 specialist agents
│   │   ├── MyPlan/SKILL.md
│   │   ├── MyPlan-Purpose/SKILL.md
│   │   ├── MyPlan-LifePlan/SKILL.md
│   │   ├── MyPlan-Goals/SKILL.md
│   │   ├── MyPlan-Habits/SKILL.md
│   │   ├── MyPlan-Daily/SKILL.md
│   │   ├── MyPlan-Energy/SKILL.md
│   │   ├── MyPlan-Motivation/SKILL.md
│   │   └── MyPlan-Review/SKILL.md
│   ├── commands/                ← Schedulable commands
│   │   ├── daily-checkin.md
│   │   ├── weekly-review.md
│   │   └── monthly-review.md
│   └── README.md                ← Plugin-specific readme
└── life-compass-data/           ← Data file templates (copy to your project)
    ├── user_profile.md
    ├── journal.md
    ├── life_plan.md
    ├── goals.md
    ├── habits.md
    ├── energy_log.md
    └── daily_plan.md
```

---

## Quick Start Commands

Once installed and onboarded, here are the most common ways to interact with MyPlan:

| Say this... | What happens |
|-------------|-------------|
| "MyPlan" | Opens the dashboard and suggests what to work on |
| "Plan my day" | Launches the Daily Pilot for morning planning |
| "Set a new goal" | Opens the Goal Architect |
| "I want to build a morning routine" | Opens the Habit Designer |
| "I feel stuck" | Opens the Motivation Coach |
| "What's my purpose?" | Opens Purpose Discovery |
| "How am I doing?" | Runs a progress review |
| "Plan my week" | Launches weekly planning |
| "I'm exhausted" | Opens the Energy Optimizer |
| "Create my life plan" | Opens the Life Planner |

---

## Contributing

Contributions are welcome. If you'd like to improve the coaching frameworks, add new agents, or enhance the data tracking, feel free to open a pull request.

---

## License

MIT License — use freely, modify as you wish, and share with others.

---

## Author

Created by **Gísli Rafn Ólafsson** — built with Claude.
