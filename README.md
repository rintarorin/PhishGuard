# PhishGuard 2026 — Hosting Guide
George Brown Polytechnic · COMP 4066 · Group 2

## Files
```
phishguard/
├── index.html        ← Home / landing page
├── quiz.html         ← 8-question phishing awareness quiz (with score tracking)
├── awareness.html    ← Campaign email template (print/copy ready)
├── dashboard.html    ← Live KPI dashboard (reads quiz scores)
├── phishguard.css    ← Shared styles (required by all pages)
└── README.md         ← This file
```

## Hosting options

### Option A — GBP Intranet / SharePoint
Upload all 5 files to a single folder. Open index.html as the entry point.
All files must stay in the same directory (CSS and links are relative).

### Option B — GitHub Pages (free, public)
1. Create a GitHub repo
2. Upload all files to the root
3. Go to Settings → Pages → Deploy from branch (main / root)
4. Your site will be live at https://yourusername.github.io/reponame/

### Option C — Netlify Drop (free, instant)
1. Go to https://app.netlify.com/drop
2. Drag the entire phishguard/ folder onto the page
3. Live in seconds — no account needed

### Option D — USB / Local
Open index.html directly in any browser. All functionality works offline
because scores are stored in browser localStorage.

## Score storage
Scores are stored in the browser's localStorage under the key `phishguard_scores`.
This means:
- Scores persist across sessions on the same browser/device
- Each device/browser has its own local scoreboard
- For a shared server-side database, the quiz.html saveScore() function
  would need to be extended to POST to a backend API

## KPI tracking
The dashboard.html page reads localStorage and shows:
- Total participants
- Average score and pass rate (≥75%)
- Per-topic performance (which questions users miss most)
- Score distribution chart
- Full scores table with CSV export

## Branding
- Primary color: Royal Blue #4169E1
- Font: Segoe UI / system-ui
- Logo: PHISHGUARD (Georgia serif)
- Tagline: "If it looks phishy — don't bite"

## Group 2
Eldrin David Asuncion · 101596358
Erasmo Lopez Villicana · 101183515
Jack Mao · 503921
Thierry Landry Kamga Tadie · 101639227
Instructor: Michael Artemio Rebultan
