# Scrum Toolkit

Static web app — single HTML file, no build process, no dependencies.
Hosted on GitHub Pages: https://jonboyle-dev.github.io/Scrum-toolkit/

## Structure
```
Scrum-toolkit/
├── index.html                  ← GitHub Pages entry (redirects to toolkit)
├── complete-scrum-toolkit.html ← Full application (all 9 tabs)
├── project-report.html
├── README.md
└── CLAUDE.md
```

## Architecture
- Single file app: all HTML, CSS, JS in `complete-scrum-toolkit.html`
- Persistence: `localStorage` only — no backend
- 9 tabs: Sprint Hub, Sprint Planning, Daily Scrum, Sprint Review, Retrospective, Sprint Poker, Ceremony Timer, Story Generator, Reference
- localStorage keys: `scrum_sprint`, `scrum_planning`, `scrum_daily`, `scrum_review`, `scrum_retro`, `scrum_skills`, `scrum_api_key`, `scrum_velocity`, `scrum_members`, `scrum_impediments`, `scrum_attendees`
- XSS protection: `san()` helper escapes all user-generated content before DOM insertion
- Story Generator API: `claude-sonnet-4-6` via Anthropic Messages API, key stored in localStorage

## Grounded in
2020 Scrum Guide (Ken Schwaber & Jeff Sutherland)

