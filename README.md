# Portfolio Generator

Build a professional portfolio website in 30 minutes using Zo — no coding required.

A **[Zo Skill](https://agentskills.io)** that walks you through building a personal website from your LinkedIn data and professional history, then deploys it live to `your-handle.zo.space`. Every step is narrated so the process itself teaches you how agentic engineering works.

## What You Get

- A polished, responsive personal portfolio
- Live at `https://your-handle.zo.space`
- Built from your real professional data (LinkedIn, resume, etc.)
- Three design directions: **Editorial**, **Technical**, **Bold**

## What You Learn

The skill narrates every step, teaching core **agentic engineering** concepts as you build:

| Concept | What It Means |
|---------|---------------|
| **Context ingestion** | Giving AI structured information to work with |
| **Human-in-the-loop** | You check the AI's work before it builds on it |
| **Context-aware generation** | AI adapts output based on who you are |
| **Iterative refinement** | The describe → build → review loop |
| **Graceful degradation** | Fallbacks when a data source fails |

## Requirements

- [Zo Computer](https://zo.computer) account
- LinkedIn profile (public, or logged into Zo's browser)
- A strong model for best results — Claude Opus/Sonnet, GPT-4o+, or Gemini 2.5 Pro+

**Optional:** Resume (PDF, DOCX, or text) · Professional headshot · Bio, achievements, or project descriptions

## Install & Run

**From the Zo skills registry:**

```bash
slug="portfolio-generator"; dest_slug="portfolio-generator"; dest="Skills"; manifest_url="https://raw.githubusercontent.com/thevibethinker/zo-skills/main/manifest.json"; mkdir -p "$dest" && tarball_url="$(curl -fsSL "$manifest_url" | jq -r '.tarball_url')" && archive_root="$(curl -fsSL "$manifest_url" | jq -r '.archive_root')" && curl -L "$tarball_url" | tar -xz -C "$dest" --strip-components=1 --transform="s|^$archive_root/$slug|$dest_slug|" "$archive_root/$slug"
```

**Or clone directly:**

```bash
git clone https://github.com/thevibethinker/portfolio-generator.git Skills/portfolio-generator
```

Then say: **"Run the portfolio generator skill"**

## How It Works

| Step | ~Time | What Happens |
|------|-------|--------------|
| Data Gathering | 5 min | Share your LinkedIn URL + optional extras |
| Profile Review | 3 min | Confirm the data Zo extracted |
| Design Direction | 3 min | Choose your aesthetic |
| Generation | 5 min | Watch Zo build and deploy your site |
| Polish | 8 min | Iterate until you love it |
| Wrap-Up | 3 min | Get your live URL and next steps |

## Example Output

Your portfolio includes:

- **Editorial-style hero** — large typography, strong professional framing
- **About section** — rewritten conversational bio
- **Experience section** — clean divider-based entries (no generic cards)
- **Skills/domains section** — clear signal, not progress bars or badge clutter
- **CTA link** — large text with animated arrow, plus a minimal footer

Additional sections (projects, certifications, education, publications) appear automatically based on your profile data.

## Skill Contents

```
portfolio-generator/
├── SKILL.md              # Main skill instructions
├── persona.md            # Vibe Onboarding persona (auto-installed)
├── scripts/
│   ├── parse_resume.py   # Resume extraction (PDF, DOCX, TXT)
│   └── validate_profile.py  # Profile data quality checks
├── references/
│   ├── design-guidelines.md  # Anti-slop design rules
│   └── teaching-moments.md   # Narration scripts
└── templates/
    └── portfolio-modern.yaml  # Design system (3 directions)
```

## Credits

Built by [V. Attawar](https://vrijenattawar.com) for [The Vibe Pill](https://thevibepill.com).
