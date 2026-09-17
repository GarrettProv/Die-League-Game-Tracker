# Sigma Chi Die League Tracker

An offline-first referee app for tracking seated Die league games.

## Run the MVP

Open `index.html` in a modern browser. For the most reliable behavior, serve the folder with a static server such as VS Code Live Server or:

```powershell
python -m http.server 8080
```

Then visit `http://localhost:8080`.

## Included features

- Unique league-wide player pool and permanent two-player teams
- Dropdown roster assignment that prevents duplicate players across teams
- League weeks
- Game setup with team, starting-team, and player-order selection
- Autosaved live games with resume support
- Automatic first-to-11, win-by-2 game completion
- Three-game series with all three games played and first-to-two series standings
- Referee-selected starting team for every game in a series
- Full throw, catch, foul, sink, rim, Social, and mug-knockover scoring
- Undo and chronological game log
- Team standings and player statistics by week or all-time
- Per-game, weekly, and overall player rankings for throw, sink, catch, and scoring performance
- Completed game history
- Weekly JSON export/import for combining games from multiple referees
- Duplicate-safe merges using unique game IDs

All data is stored in the browser's local storage. Clearing site data will remove it, so export weekly files as backups.

## Multi-referee workflow

1. One person creates the teams and current week, then exports the week file.
2. Every referee imports that file before games begin so player/team IDs match.
3. Referees track games independently on their devices.
4. Each referee exports their week file.
5. The commissioner imports all files. Duplicate games are skipped automatically.

Planning and rule details are in `APP-PLAN.md` and `THROW-STATS-PLAN.md`.
