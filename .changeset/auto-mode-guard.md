---
"mattpocock-skills": patch
---

Interview skills now stop when the session is in auto mode. `grilling` (and so `grill-me` and `grill-with-docs`), `setup-matt-pocock-skills`, `to-tickets`, `to-questionnaire`, `wayfinder` (charting and human-in-the-loop tickets only) and `teach` (only when the mission needs asking) ask nothing, assume nothing and write nothing, and tell the user to switch auto mode off and run them again. In Claude Code the signal is the `## Auto Mode Active` system reminder; a harness with no signal still asks and waits. `grill-with-docs` now runs `grilling` before `domain-modeling`, so a stop also stops the docs.
