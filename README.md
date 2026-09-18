**Currently in beta testing only, and repo not available publicly.**

# Lets-Land-It-Public
A website for automatically highlighting the key areas of your resume as they relate to a specific job posting.


Land-It

AI-powered job application assistant. Land-It helps job seekers track every application while automatically tailoring their resume and cover letter to each role — enriched with live company research and a full interview prep package.

🌐 letslandit.co

Every application, polished. Every interview, prepared.

What it does

Paste a job posting (or drop in a URL). Land-It generates:

✦ Tailored resume — your experience rewritten to match the role's keywords and priorities
✦ Custom cover letter — specific to the company, role, and your background
✦ Company intel — recent news, funding, product launches, and industry trends
✦ Interview prep — curated videos, articles, and likely questions inferred from the job description

All of it tracked in one place, organized by application status.

Status

🟢 In development — auth working, staging live at test.letslandit.co

Features
Core loop
Sign up and share your resume once (PDF upload or paste)
Add a job — paste the description or drop in a URL
Get a full application package in ~15 seconds
Track status: Saved → Applied → Interview → Offer → Rejected
Resume versions
Maintain multiple resume variants optimized for different role types or industries
Land-It picks the best base for each application and tailors it further
Export any version as PDF
LinkedIn integration (planned)
Import your LinkedIn profile as your resume
Pull in jobs you've already applied to
Application tracker
Status tracking per application
Notes field
Cover letter and prep package status indicators
Tech stack
Layer	Choice
Frontend	React + Vite
Auth + Database	Supabase
AI	Anthropic API (Claude Sonnet)
Job scraping	Jina.ai or Firecrawl (planned)
PDF export	React-PDF (planned)
Hosting	Vercel
Domain	letslandit.co via GoDaddy
Development workflow

Local:

bash
npm run dev
# runs at http://localhost:5173

Deploy to staging:

bash
git checkout test
git add .
git commit -m "your changes"
git push origin test
# auto-deploys to test.letslandit.co

Deploy to production:

bash
git checkout main
git merge test
git push origin main
# auto-deploys to letslandit.co
Project structure
Land-It/
├── src/
│   ├── App.jsx          # Main app — all screens and navigation
│   ├── supabase.js      # Supabase client
│   └── main.jsx         # Entry point
├── docs/
│   └── requirements.md  # Full product requirements
├── CLAUDE.md            # Claude Code project context
├── NOTES.md             # Session notes and next steps
└── README.md
Roadmap
 UI prototype — all screens, full navigation
 Auth — sign up, login, logout via Supabase
 Staging deployment — test.letslandit.co
 Resume parsing and storage (Supabase)
 Cover letter generation (Anthropic API)
 Resume tailoring (Anthropic API)
 Company intel via web search
 Interview prep bundle
 PDF export
 LinkedIn import
Docs
docs/requirements.md — full product requirements and screen specs
