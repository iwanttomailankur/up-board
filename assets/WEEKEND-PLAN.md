# UP Board Class 12 Physics — Weekend Build Plan

## What you have now
A working static site (`index.html`, `about.html`, `contact.html`, `privacy-policy.html`, `assets/style.css`) with:
- All 9 official UPMSP Physics units, correctly split into Part A (35 marks) and Part B (35 marks)
- A placeholder slot on every unit card ready for a YouTube embed
- 3 ad slots pre-placed (top, mid, bottom) — currently empty divs, ready for AdSense `<ins>` codes once approved
- The 3 pages AdSense reviewers expect to see (About, Contact, Privacy Policy)

Open `index.html` in a browser right now to see it live — no build step needed.

## Saturday — content
1. **Script each unit (aim: all 9, ~20–30 min each incl. review)**
   - Feed the unit's NCERT chapter + UPMSP syllabus points into NotebookLM
   - Use it to generate a structured explainer script — treat it as a first draft, tighten the language yourself so it teaches rather than just narrates
2. **Build one reusable video template**
   - Intro card (5 sec): unit number + name + marks weightage
   - Slides: 1 per major concept, formulas called out visually
   - Outro: "next unit" card linking the sequence together
   - Do this once, reuse for all 9 — don't redesign per video
3. **Record/assemble 2–3 pilot videos** to validate the template before batching the rest

## Sunday — publish + wire up
1. **Upload to YouTube**
   - Title format: `Class 12 Physics Unit [N]: [Unit Name] | UP Board 2027`
   - Run each title/description through vidIQ before publishing (you already have this connected) — worth doing per-unit since Physics keyword competition is high
   - Group all 9 into one Playlist
2. **Wire videos into the site**
   - For each unit card in `index.html`, replace the placeholder `<div class="placeholder">` block with the commented-out `<iframe>` line, and swap in your real `VIDEO_ID`
3. **Finish the compliance pages**
   - `contact.html` — put your real email
   - `privacy-policy.html` — confirm it matches what you'll actually run (analytics, cookies)
4. **Deploy**
   - Push to GitHub Pages (free) — see deploy notes below
   - If you want AdSense to approve smoothly, point a real domain at it (₹700–1,000/yr from any registrar) rather than the free `github.io` subdomain — not required, but approval odds and ad rates are both better on a real domain
5. **Apply to AdSense** once at least a handful of units are live with real content (not just embeds — the topic summaries on each card already give you original text, which helps)

## Realistic sequencing on money
- AdSense review typically takes days to a couple of weeks — apply once the pilot is live, don't wait for all 9 units
- Website ad income scales with traffic, which takes months to build for a new site — SEO from the unit names/topics already on the page helps, but this isn't a weekend outcome
- YouTube's own ad revenue (Partner Program) needs 1,000 subscribers + 4,000 public watch hours in 12 months — separate milestone from the site

## Deploy notes (GitHub Pages, free)
1. Create a new GitHub repo, e.g. `up-board-physics`
2. Upload all files in this folder (keep the `assets/` folder structure intact)
3. Repo Settings → Pages → Deploy from branch → `main` → `/root`
4. Site goes live at `https://yourusername.github.io/up-board-physics/`
5. Optional: buy a domain and point it at GitHub Pages via a CNAME file (ask if you want the exact steps when you're ready)

## Next subject after Physics
Once this pattern is proven, Chemistry and Biology reuse the same template — only the unit list and video content change. Maths can follow the same pattern but note it has no practical component (100 marks, theory-only).
