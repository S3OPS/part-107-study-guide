# Part 107 FAA Exam Study Guide

A free, interactive study aid for the FAA Part 107 Remote Pilot knowledge test (UAG) — **192 practice questions with explanations**, a timed exam simulator, flashcards, and targeted weak-area review. It runs as a single HTML file in any modern browser: no account, no install, no backend.

**▶ Use it live:** [Landing page](https://s3ops.github.io/part-107-study-guide/) · [Open the study guide directly](https://s3ops.github.io/part-107-study-guide/part107-study-guide.html)

> **Accuracy note:** This is an independent study aid. It is not published by, affiliated with, or endorsed by the FAA, and it does not guarantee a passing score. The question bank was reviewed against 14 CFR Part 107 and FAA guidance in November 2026 (see *Content review* below). Regulations change — always confirm current requirements with the FAA before relying on an answer operationally.

## What it does

- **Practice Mode** — answer at your own pace with instant feedback and an explanation for every question; filter by category, search by keyword, bookmark questions, and review only your bookmarks or only the questions you missed.
- **Exam Simulator** — 60 questions against a 2-hour countdown, matching the format of the real UAG test (60 questions, 2 hours, 70% to pass, at an FAA-approved testing center), with a per-category results breakdown and one-click weak-area drills.
- **Flashcard Mode** — flip-card active recall; mark cards “Know It” or “Need Review.”
- **Progress that persists** — sessions, scores, bookmarks, and performance history are stored locally in your browser (localStorage), so you can stop and resume on the same device.
- **Reference material** — sectional-chart and Chart Supplement visual guides, an airspace quick reference, key Part 107 facts, test-day strategies, and links to official FAA resources.

## Question bank

| Category | Questions |
| --- | ---: |
| Airspace Classification & Chart Reading | 40 |
| Regulations & Operating Requirements | 25 |
| Weather | 22 |
| Emergency Procedures | 14 |
| Decision Making | 13 |
| Maintenance & Preflight | 13 |
| Crew Resource Management | 12 |
| Night Operations | 12 |
| Loading & Performance | 11 |
| Operations | 10 |
| Radio & Airport Operations | 10 |
| Operations Over People | 10 |
| **Total** | **192** |

Every question has four options, one verified answer key, and a written explanation.

## Content review — November 2026

The bank was audited before this README was rewritten:

- **Structural validation (automated):** all 192 questions parse cleanly; every answer key points at a valid option; every question has an explanation; category counts above were recomputed from the bank itself; no exact duplicate questions.
- **Regulatory review (manual, against primary sources):** the rules-facing questions were checked against the current text of [14 CFR Part 107](https://www.ecfr.gov/current/title-14/chapter-I/subchapter-F/part-107) (eCFR, current to November 2026), 14 CFR Part 48 (registration and marking), 14 CFR Part 89 (Remote ID), and the FAA's [Become a Drone Pilot](https://www.faa.gov/uas/commercial_operators/become_a_drone_pilot) guidance.
- **Corrections made in this pass (22 questions):** the most significant were —
  - **Certificate “renewal”** — the Remote Pilot Certificate does not expire; §107.65 requires recurrent *training* within the previous 24 calendar months. Two questions taught the old framing (and one referenced a recurrent knowledge test that no longer exists); all are corrected.
  - **Registration** — one question applied the 0.55 lb recreational threshold to Part 107. Under Part 107, *every* aircraft must be registered regardless of weight.
  - **Operations over moving vehicles** — three questions misstated §107.145. Category 1–3 operations may avoid sustained flight over vehicles, or conduct it within/over a closed- or restricted-access site with the occupants on notice.
  - **Night operations** — corrected to §107.29 as written: a post–April 6, 2021 knowledge test or training covering night operations, plus anti-collision lighting visible for at least 3 statute miles. An unsupported “360 degrees” lighting claim was removed.
  - **Remote ID** — clarified standard Remote ID vs. broadcast-module message elements and the FRIA exception (§89.120).
  - **§107.51** — the section covers groundspeed, altitude, flight visibility, and distance from clouds (visual line of sight is §107.31; night is §107.29).
  - Two duplicate questions (minimum age; maximum weight) were replaced with distinct questions on §107.61 English-language eligibility and Part 48 exterior marking.
- **Copy softening:** absolute claims (“covers everything,” “actual exam distribution,” pass guarantees) were replaced with sourced, qualified language, and the app now carries the accuracy note above on its start screen.

Weather, aerodynamics, and airmanship content follows standard FAA study material (Pilot's Handbook of Aeronautical Knowledge; FAA Remote Pilot Study Guide, FAA-G-8082-22). Spotted an error? Open an issue with the question text and an FAA source — corrections are welcome.

## Run it locally

Download `part107-study-guide.html` and open it in a browser. That's it. Optional: serve the folder (`python3 -m http.server`) and open `index.html` for the landing page.

## Technical notes

- Single-file app (`part107-study-guide.html`, ~470 KB): markup, styles, question bank, and logic in one file, so it can be shared or hosted anywhere static files can go.
- Charts use Chart.js from a CDN with a built-in canvas fallback if the CDN is unreachable.
- All user data stays in the browser's localStorage; nothing is sent anywhere.
- `index.html` is a static landing page that links to the app.

## Status

Maintained as a free resource alongside [Second Sight Solutions](https://github.com/S3OPS/secondsightsolutions), a veteran-owned drone services project in Central Texas.
