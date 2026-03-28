---
description: Run your daily MyPlan check-in (morning planning or evening review)
allowed-tools: Read, Write, Edit, Glob, Grep
---

Run a daily check-in for the MyPlan life planning system. This command supports both morning planning and evening review.

First, determine the time of day and context:
- If it's morning or the user says "plan my day", run a **Morning Planning** session
- If it's evening or the user says "review my day", run an **Evening Review** session
- If unclear, ask the user which they'd prefer

Read these files for context:
- `life-compass-data/user_profile.md` (name, chronotype, preferences)
- `life-compass-data/goals.md` (active goals and lead measures)
- `life-compass-data/habits.md` (habits to track today)
- `life-compass-data/daily_plan.md` (existing plans)
- `life-compass-data/journal.md` (last 30 lines for recent context)

Check the user's preferred check-in mode from their profile:
- **Quick Report mode**: Generate a brief status report, highlight today's priorities, list habits to complete, and ask 2 targeted questions
- **Guided Conversation mode**: Walk through planning/review conversationally, one question at a time

**Morning Planning:**
1. Greet the user by name warmly
2. Ask about their energy level (1-10)
3. Review what goals need attention this week
4. Help identify today's Big 3 priorities
5. Confirm daily habits to maintain
6. Write the plan to `life-compass-data/daily_plan.md`

**Evening Review:**
1. Ask: What were your wins today?
2. Ask: What didn't get done (and why)?
3. Ask: What's your biggest takeaway?
4. Ask: What are you grateful for?
5. Confirm: What's tomorrow's #1 priority?
6. Check habit completion for the day
7. Update `life-compass-data/daily_plan.md` with the reflection
8. Log to `life-compass-data/journal.md`

Use a warm, encouraging coaching tone. Celebrate wins genuinely. Be brief — this is a daily tool.
