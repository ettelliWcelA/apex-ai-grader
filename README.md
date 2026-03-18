# APEX·AI — Quantitative AI Stock Grader

![APEX·AI v5.0](https://img.shields.io/badge/APEX·AI-v5.0-00d4ff?style=for-the-badge&labelColor=060810)
![Powered by Claude](https://img.shields.io/badge/Powered_by-Claude_AI-a060ff?style=for-the-badge&labelColor=060810)
![AI Sector Only](https://img.shields.io/badge/Scope-AI_Sector_Only-30f090?style=for-the-badge&labelColor=060810)
![No Build Required](https://img.shields.io/badge/Setup-Zero_Config-f0c040?style=for-the-badge&labelColor=060810)

> A 12-factor quantitative grading system for AI-sector stocks, powered by the Claude API. Enter any ticker — APEX·AI researches the company and delivers a full investment scorecard in seconds.

---

## What is APEX·AI?

APEX·AI v5.0 is a **12-factor quantitative stock grading model** built for the AI investment era. It combines classic fundamental analysis with four proprietary "Navellier Stage 2" factors — designed to surface the difference between hype-driven narratives and genuine AI compounders.

The system grades stocks on a **0–100 composite score** with a **85+ buy threshold**, producing a full scorecard including:

- Weighted factor breakdown with visual bars
- Navellier Stage 2 analysis (Feedback Loop, Stage 2 Position, Physical AI, Institutional Alpha)
- AI-generated investment thesis and key risks
- Letter grade (A+ through C) and recommendation
- Analyst upside estimate

**AI Sector Constraint:** APEX·AI exclusively grades companies with meaningful AI exposure. Non-AI stocks are rejected with an explanation.

---

## Live Demo

**[▶ Try APEX·AI on GitHub Pages →](https://ettelliWcelA.github.io/apex-ai-grader)**

*(Update this link after deploying — see Setup below)*

---

## The 12 Factors

### Original Factors (70% weight)

| # | Factor | Weight | What It Measures |
|---|--------|--------|-----------------|
| 1 | **AI Revenue Exposure** | 16% | % of revenue from AI products/infrastructure |
| 2 | **Earnings Momentum** | 13% | EPS beat cadence, analyst revisions, acceleration |
| 3 | **Revenue Growth** | 11% | YoY/QoQ growth, forward CAGR, TAM penetration |
| 4 | **Economic Moat** | 11% | IP, network effects, switching costs, data moat |
| 5 | **Quantitative Momentum** | 9% | Price momentum vs. S&P 500 and sector peers |
| 6 | **Balance Sheet Quality** | 6% | Debt/equity, cash position, FCF yield |
| 7 | **Management & Execution** | 4% | R&D%, insider ownership, guidance accuracy |

### Navellier Stage 2 Factors (30% weight) ★ NEW in v5.0

| # | Factor | Weight | What It Measures |
|---|--------|--------|-----------------|
| 8 | **Feedback Loop Velocity** | 9% | Self-reinforcing data flywheel — does the product make itself smarter? |
| 9 | **Stage 2 Position** | 8% | Overlooked real-earnings compounder vs. fully-priced hype stock |
| 10 | **Physical AI Embodiment** | 7% | AI translating into robots, vehicles, surgical systems, sensors |
| 11 | **Institutional Alpha Signal** | 6% | Smart money accumulating before it becomes consensus |

### Grade Scale

| Grade | Score Range | Recommendation |
|-------|------------|----------------|
| **A+** | 92–100 | Strong Buy |
| **A**  | 86–91  | Buy |
| **B+** | 80–85  | Selective Buy |
| **B**  | 74–79  | Watchlist |
| **C+** | 68–73  | Hold / Pass |
| **C**  | 0–67   | Avoid |

> **Buy threshold: 85+.** Only stocks scoring 85 or above are considered for portfolio inclusion.

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | Pure HTML5 / CSS3 / Vanilla JS |
| AI Engine | Claude API (`claude-sonnet-4-20250514`) |
| Deployment | GitHub Pages (static, no server) |
| Build System | None — zero config |
| Dependencies | Google Fonts CDN only |

**Why no framework?** Zero dependencies means zero maintenance, zero security vulnerabilities from npm packages, and instant deployment anywhere. The entire app is one `index.html` file.

---

## Setup & Deployment

### Option A: Run Locally (30 seconds)

```bash
# 1. Clone the repo
git clone https://github.com/YOUR-USERNAME/apex-ai-grader.git

# 2. Open in your browser — no server needed
open apex-ai-grader/index.html
# or just double-click index.html in Finder / File Explorer
```

### Option B: Deploy to GitHub Pages (free hosting, ~2 minutes)

See the full [GitHub Setup Guide](#github-setup-guide) below.

### Getting an Anthropic API Key

1. Go to **[console.anthropic.com](https://console.anthropic.com)**
2. Create an account or sign in
3. Navigate to **API Keys** → **Create Key**
4. Copy the key (starts with `sk-ant-api03-...`)
5. Paste it into the APEX·AI input field

> **Security note:** Your API key is used directly in your browser via the Anthropic API. It is never sent to any third-party server, never logged, and never stored beyond your browser session. The app has no backend.

---

## GitHub Setup Guide

### Step 1 — Create your GitHub account
If you don't have one: go to **[github.com](https://github.com)** → Sign up (free).

### Step 2 — Create a new repository

1. Click the **+** icon (top right) → **New repository**
2. Name it: `apex-ai-grader`
3. Set to **Public** (required for free GitHub Pages)
4. ✅ Check **"Add a README file"** — uncheck this if you're uploading our README
5. Click **Create repository**

### Step 3 — Upload the files

**Method A — GitHub web interface (easiest, no Git required):**

1. On your new repository page, click **"uploading an existing file"** or drag-and-drop
2. Upload all files:
   - `index.html`
   - `README.md`
   - `.gitignore`
   - `LICENSE`
3. In the commit message box, type: `Initial release — APEX·AI v5.0`
4. Click **Commit changes**

**Method B — Git command line:**

```bash
# Clone your empty repo
git clone https://github.com/YOUR-USERNAME/apex-ai-grader.git
cd apex-ai-grader

# Copy the APEX·AI files into this folder
# (index.html, README.md, .gitignore, LICENSE)

# Stage, commit, and push
git add .
git commit -m "Initial release — APEX·AI v5.0"
git push origin main
```

### Step 4 — Enable GitHub Pages

1. In your repository, click **Settings** (top tab)
2. In the left sidebar, click **Pages**
3. Under **Source**, select **Deploy from a branch**
4. Branch: **main** | Folder: **/ (root)**
5. Click **Save**
6. Wait ~60 seconds, then your live URL will appear:
   `https://YOUR-USERNAME.github.io/apex-ai-grader`

### Step 5 — Update your README

Replace `YOUR-USERNAME` in the Live Demo link at the top of `README.md` with your actual GitHub username, then commit the change.

---

## Project Structure

```
apex-ai-grader/
├── index.html      ← Complete app (single file)
├── README.md       ← This file
├── .gitignore      ← Standard web ignores
└── LICENSE         ← MIT License
```

---

## Example Stocks to Grade

These AI-sector stocks work well with APEX·AI:

**Semiconductors:** `NVDA` `AVGO` `AMD` `TSM` `MU` `SNDK`  
**AI Cloud/Infrastructure:** `MSFT` `GOOGL` `AMZN` `META` `NBIS`  
**AI Software:** `PLTR` `ORCL` `CRM` `PATH`  
**Physical AI / Robotics:** `ISRG` `SYM` `TSLA`  
**AI Networking:** `ANET`  
**AI Power:** `GEV`

**Non-AI stocks** (will be rejected by the AI sector filter): `KO` `JPM` `WMT` `XOM`

---

## Methodology Notes

- **Score calibration:** Scores are intentionally conservative. A 95+ on any factor is reserved for best-in-class, verifiable, durable leaders. Score inflation is the #1 grader error.
- **Composite formula:** `Σ (factor_score × weight/100)` across all 11 factors
- **AI-generated data:** All factor scores and analysis are generated by Claude AI based on its training knowledge. Always verify key numbers from primary sources (SEC filings, earnings reports) before making investment decisions.
- **Threshold:** The 85-point buy threshold is a screening guideline, not a buy signal. It indicates sufficient quality across the 12-factor framework to merit further research.

---

## Disclaimer

APEX·AI is an educational tool built to demonstrate quantitative investment research methodology. It does **not** constitute financial advice. All scores and analysis are AI-generated and may contain inaccuracies or outdated information. Always verify data from primary sources. Past performance does not guarantee future results. Investing involves risk of loss. Consult a licensed financial advisor before making investment decisions.

---

## License

MIT License — see [LICENSE](LICENSE) for details.

---

*Built with the [Anthropic Claude API](https://anthropic.com) · APEX·AI v5.0 · 12-Factor Quantitative Model*
