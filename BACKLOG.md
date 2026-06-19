# Scrum Toolkit — Backlog & Discussion Items

## 🔵 To Discuss

### Remove API key requirement from Story Generator
**Context:** The Story Generator currently requires each user to supply their own Anthropic API key because the app calls the API directly from the browser (no backend). Baking a key into the HTML would expose it publicly.

**Option on the table:** Cloudflare Worker as a thin proxy — one file, free tier covers millions of requests/month, key stays server-side. Trade-off: breaks the single-file, zero-infra goal.

**Questions to resolve:**
- Who is the intended audience? Internal team only, or public?
- Are we OK adding a minimal piece of infra (Cloudflare Worker)?
- Should usage be rate-limited or authenticated?

---

## ✅ Done

- [x] Left sidebar navigation
- [x] Home dashboard with role-based personalisation (SM / Dev / PO)
- [x] Hamburger menu for mobile
- [x] Story Generator — improved API key UX (explanation + link to console)
