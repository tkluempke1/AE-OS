# AE-OS# Docker AE Operating System

A self-contained, single-file sales productivity app built for Docker Account Executives. Access sales frameworks, prospecting templates, account intelligence, and deal strategy tools — all from one HTML file that works anywhere, offline, with zero setup.

## Why This Exists

AEs spend 30-60 minutes per day searching through scattered documents for frameworks, templates, and account intel. This app puts everything in one searchable, instant-access tool:

- **MEDDPICC questions** — 2 clicks instead of digging through a 250-page playbook
- **Prospecting templates** — Copy-paste ready with placeholders, organized by industry and urgency
- **Account intelligence** — 25 priority accounts with named contacts, sequences, and deal strategies
- **Deal tools** — ROI calculator, champion validation, stage readiness, and more

## Quick Start

1. Download `docker-ae-os.html`
2. Double-click to open in any browser
3. That's it — no installation, no server, no internet required

## Features

### Framework Reference Library
Complete, interactive reference for core sales methodologies:
- **MEDDPICC** — All 8 elements with discovery questions, red flags, and examples
- **Command of the Message** — Value drivers, before/after scenarios, differentiation
- **Champion Building** — 4-stage framework (Identify, Build, Test, Use)
- **The 4 Why's** — Why Docker? Why Now? Why You? Why This Approach?
- **Sales Process Stages (S0-S4)** — Exit criteria and MEDDPICC requirements by stage

Each framework includes copy-to-clipboard questions, cross-links to related templates and tools, and a sticky "Jump to" sub-navigation.

### Template Library
20+ copy-paste ready templates organized by category:
- **Prospecting emails** — By urgency (compliance, post-incident, M&A, cloud transformation) and industry
- **Discovery question banks** — Organized by MEDDPICC element, role, and sales stage
- **Objection handlers** — Scripts for the 5 most common objections with reframing tactics
- **Multi-touch sequences** — Complete outreach cadences with timing and channel mix

All templates have one-click copy, placeholder highlighting, and filterable search.

### Account Intelligence Hub
25 priority accounts with detailed case studies:
- Company profile, developer count, ARR, TAM
- Compelling events and pain points
- Named executive contacts with role-specific approaches
- Full prospecting sequences (5-7 touches per account)
- MEDDPICC-mapped discovery questions
- Org chart visualization with champion/EB identification
- Competitive landscape and procurement intelligence
- Replicable playbook patterns applicable to any account

Filterable by industry, tier, and keyword search.

### AE Tool Hub
Interactive deal planning tools:
- **MEDDPICC Intake** — Guided qualification form with field validation and SFDC-ready output
- **ROI Calculator** — Productivity, security, and compliance savings with formatted talking points
- **Champion Validation** — 4-stage checklist with scoring and recommendations
- **Multi-Threading Strategy** — Contact mapping and outreach planning
- **Deal Health Scorecard** — Weighted assessment with improvement recommendations
- **Stage Readiness Checker** — Exit criteria verification before advancing deals
- **Competitive Battle Cards** — Side-by-side positioning against alternatives
- **Manager 1:1 Prep** — Generate pipeline review summaries from deal health scores

Tools render inline with breadcrumb navigation when accessed from the hub, or as modals when accessed from search/cross-links.

### Smart Search
Type questions in natural language from anywhere in the app:
- Contextual recommendations (e.g., "how do I qualify a deal?" surfaces MEDDPICC)
- Keyword search across all frameworks, templates, accounts, and tools
- Search result highlighting with animated scroll-to on navigation
- Keyboard shortcut: press `/` to focus search from anywhere

### Additional Features
- **Onboarding tour** — First-time walkthrough with spotlight highlights
- **Recently accessed** — "Pick up where you left off" section on dashboard
- **Shared Deal Context** — Fill out MEDDPICC once, auto-populates across all tools
- **localStorage persistence** — Saved MEDDPICC entries, deal health scores, and tool outputs
- **URL hash routing** — Deep-link to any section (e.g., `#accounts`, `#deal-strategy/roi-calculator`)
- **Cross-linking** — Related content links between frameworks, templates, and tools
- **Responsive design** — Works on desktop, tablet, and mobile
- **Print-friendly** — Clean print styles for frameworks and templates
- **Keyboard accessible** — Full keyboard navigation and ARIA labels

## Tech Stack

| Component | Choice | Why |
|-----------|--------|-----|
| HTML/CSS/JS | Vanilla, no frameworks | Zero dependencies, instant load, works everywhere |
| Architecture | Single file | Easy distribution, no build step, no server needed |
| Data | Embedded JSON | All content self-contained, works offline |
| Storage | localStorage | Persists user data without a backend |
| Styling | CSS Grid + Flexbox + Custom Properties | Modern, responsive, no CSS framework needed |

**File size:** ~993 KB | **Lines:** ~13,900 | **Load time:** < 1 second

## Browser Support

| Browser | Supported |
|---------|-----------|
| Chrome | Yes |
| Safari | Yes |
| Firefox | Yes |
| Edge | Yes |

## Deployment Options

### Option 1: Direct file sharing (Simplest)
Send `docker-ae-os.html` via Slack, email, or shared drive. AEs download and double-click.

### Option 2: GitHub Pages (Recommended for teams)
```bash
# Push to a GitHub repo with Pages enabled
git add docker-ae-os.html
git commit -m "Deploy AE OS v1.7"
git push

# AEs bookmark the Pages URL — always get the latest version
```

### Option 3: Any static hosting
Upload to S3, Netlify, Vercel, or any internal web server. It's just one HTML file.

### Option 4: Docker container (on-brand)
```dockerfile
FROM nginx:alpine
COPY docker-ae-os.html /usr/share/nginx/html/index.html
EXPOSE 80
```
```bash
docker build -t ae-os .
docker run -p 8080:80 ae-os
# Open http://localhost:8080
```

## Updating

To release a new version:
1. Edit `docker-ae-os.html`
2. Update the version number in the footer (search for `v1.7`)
3. Redistribute via your chosen method

AEs replace their local copy or refresh the hosted URL — no migration needed.

## Project Structure

```
.
├── docker-ae-os.html          # The complete app (single file)
├── docker-mark-blue (1).svg   # Docker logo SVG source
└── README.md                  # This file
```

Everything else in the directory is build artifacts and backups from development — only `docker-ae-os.html` is needed for distribution.

## Built With

Built with [Claude Code](https://claude.ai/claude-code) — from initial architecture through all 36 enhancement items across 5 implementation waves.

## License

Internal Docker Inc. sales tool. Not for external distribution.
