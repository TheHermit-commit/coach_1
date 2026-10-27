# Tempo Coach — AI training & food coach

An adaptive coach for athletes in any sport (or several at once). The athlete describes their goals in their own words, and the Coach builds a periodized plan, adjusts it from daily check-ins, plans meals and reviews what they ate.

**Live app:** https://claude.ai/artifact/Ws8BZCEezaY4yn3ssCSHjK

## Features

- **Onboarding** — age, height, weight, sports (18 to choose from, or your own), a free-text goal per sport, schedule, and dietary preferences.
- **One combined training plan** for all sports, with a sport switcher to view each sport's goal, progress tests and sessions.
- **Daily check-ins in plain language** ("legs heavy, slept 5 hours, knee ache") — the Coach adjusts the next 7 days and explains every change.
- **Injury flags** — phrases that can signal injury are caught on the device and by the Coach, with a clear "see a physio" warning.
- **Exercise videos** — a drop-down on today's workout with a YouTube search link for each exercise or drill.
- **Progress** — weekly training load (minutes × effort), load ratio warnings, energy trend, and pattern analysis.
- **Food** — daily calorie and macro targets from body stats and that day's training, meal plans, plain-language food logging with a review and tips for tomorrow, and a 4-week tracker of days logged and days at 80%+ of target.
- **Coach chat** that sees the athlete's plan, workouts, food and check-ins.

## How it runs

`index.html` is a single self-contained file (plain HTML, CSS and JavaScript, no build step).

The AI features and account storage come from the claude.ai artifact runtime (`window.claude`), so they only work when the page is opened through its claude.ai link while signed in. Opened as a plain file or from another host, the app still loads, shows the example athlete and keeps data in the browser's local storage, but the Coach can't answer.

Running it fully standalone would need a small backend that calls the Anthropic API with your own API key (never put a key in this file).

## Disclaimer

Training loads, calorie targets and injury warnings are estimates and general guidance, not medical or dietetic advice.
