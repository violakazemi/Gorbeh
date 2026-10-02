# Gorbeh 🐱

A small goal tracker with a cat who cares whether you showed up today.

*Gorbeh* (گربه) is Persian for "cat." The app turns one big goal into a daily plan, keeps a streak, and has a mascot whose mood follows your progress. I built it for my own goal: land one interview by October 31.

**Open it:** https://violakazemi.github.io/gorbeh/

## What it does

- **Daily plan.** Each day has a short list of tasks grouped into morning, deep work, and wrap-up. Weekdays, Saturdays, and Sundays each have their own plan.
- **Streak.** A day counts only when every core task is done. Partial days don't break anything, they just don't add to the streak.
- **XP.** Every task earns points, with a big bonus for reaching the goal itself.
- **Gorbeh's mood.** Happy in the morning, worried in the evening if tasks are still open, proud when the day is complete.
- **Pipeline.** Log each application and outreach message, track its status, and see which threads need a follow-up.
- **To-dos.** One-off tasks that carry over to the next day until they're done.
- **Schedule and calendar.** Today's timeline with a "now" marker, plus a month view of completed days.
- **Anchor.** A daily reminder to read your own "why" before the laptop opens.
- **Daily report.** A summary of the day, with a "what I shipped" note, ready to email or copy.

## How it works

Gorbeh is a single HTML file with no build step, no framework, and no server.

- **Your data stays on your device.** Everything is saved in the browser's `localStorage`. There is no account and nothing is uploaded.
- **Works offline.** A service worker caches the app after the first visit.
- **Installs like an app.** It ships a web manifest and icons, so it can live on a phone's home screen.

## Install on your phone

1. Open the link above in Safari (iPhone) or Chrome (Android).
2. iPhone: tap **Share**, then **Add to Home Screen**. Android: open the menu, then tap **Install app**.
3. Open Gorbeh from the home screen.

Progress is stored per browser and per device. Clearing site data resets it.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app: markup, styles, and logic |
| `sw.js` | Service worker for offline use |
| `manifest.webmanifest` | App name, colors, and icons for installing |
| `icon-180.png`, `icon-192.png`, `icon-512.png` | Home screen icons |

## Updating

1. Replace `index.html` with the new version.
2. In `sw.js`, raise the cache name (for example `gorbeh-v16` to `gorbeh-v17`) so phones pick up the new files.
3. Commit, then close and reopen the app.

## Make it yours

The plan lives near the top of the script in `index.html`:

- `TASKS` holds the daily tasks, their XP, and which ones count for the streak.
- `SCHED` holds the timeline for each kind of day.

Change those two and you have a tracker for a different goal.

## Credits

Designed by [Viola Kazemi](https://violakazemi.com). Built with Claude.
