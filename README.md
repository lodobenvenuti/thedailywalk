# The Daily Walk - Weekly Workout Protocol

A simple, static weekly workout protocol display. Shows a 7-day training split with AM/PM sessions.

## Structure

```
data/weekly-protocol.json   # Workout data (edit this to update the plan)
index.html                  # UI (loads data from JSON)
```

## Usage

Serve the directory with any static file server:

```bash
npx serve .
# or
python3 -m http.server 8000
```

Then open `http://localhost:3000` (or `8000`).

## Updating the Protocol

Edit `data/weekly-protocol.json`. The structure supports:

- **day** — Day of the week
- **sessions[]** — Array of training sessions
  - **time** — `"AM"` or `"PM"`
  - **title** — Session name
  - **category** — `"cardio"`, `"strength"`, or `"conditioning"`
  - **exercises[]** — List of exercises with optional `sets`, `distance`, `duration`
- **rest** — Set to `true` for rest days
