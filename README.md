# CKA Grind

A single-file, offline-capable study app for the Certified Kubernetes Administrator (CKA) exam, aligned to the v1.35 curriculum (post-Feb-2025 revamp).

- **Course** — six modules weighted like the real exam domains, each gated by a test at 85% (real exam bar is 66%).
- **Drill** — flashcard decks per module; missed cards recycle until cleared.
- **Final** — 30-question domain-weighted readiness exam with a 30-minute timer, unlocked once every module test is passed.
- **Setup** — lab environment instructions (killercoda, kind, kubeadm VMs) and exam logistics.

Progress is saved in the browser's localStorage (per device). Use **Setup → Copy/Paste progress code** to carry progress between devices.

No build step, no dependencies — `index.html` is the whole app.
