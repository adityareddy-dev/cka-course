# CKA Grind

A single-file, offline-capable study app for the Certified Kubernetes Administrator (CKA) exam, aligned to the v1.35 curriculum (post-Feb-2025 revamp).

- **Course** — six modules weighted like the real exam domains, each gated by a test at 85% (real exam bar is 66%).
- **Drill** — flashcard decks per module; missed cards recycle until cleared.
- **Final** — 30-question domain-weighted readiness exam with a 30-minute timer, unlocked once every module test is passed.
- **Setup** — lab environment instructions (killercoda, kind, kubeadm VMs) and exam logistics.

## Progress tracking

Progress saves to the browser's localStorage and, when a GitHub token is set in **Setup → Cloud sync**, auto-commits to [`progress.json`](progress.json) in this repo (devices without the token still pull it on load; **Setup → Sync fallback** covers the rest by copy-paste code).

**For AI assistants / study chats:** read the current progress at any time from
`https://raw.githubusercontent.com/adityareddy-dev/cka-course/master/progress.json`
(raw CDN may lag ~5 min). Fields: `tests.m1..m6` hold `best` (percent) and `attempts` per module test, `final` likewise for the 30-question readiness exam, `streak` is consecutive study days, `updated` is a ms epoch of the last change, and `summary` is a prebuilt human-readable one-liner. Module tests pass at 85%; all six passed unlocks the final; final at 85%+ means book the real exam.

No build step, no dependencies — `index.html` is the whole app.
