# TF154 — Source of Truth

**Task Force 154 / Reaper Six** — Primary project repository.

This repo is the canonical Source of Truth (SoT) for all assets, content, code, and documentation related to Task Force 154 and the Reaper Six book series.

---

## Repository Structure

```
TF154/
├── .github/
│   └── workflows/
│       └── validate.yml       # Auto-validates repo structure on every push
├── assets/                    # Shared images, documents, misc assets
├── audio/                     # Audio assets and soundscapes
├── book/                      # Reaper Six manuscript, chapters, cover art
├── brand/                     # Logos, favicons, color palettes, style guides
├── docs/                      # Knowledge base, lore bible, editorial notes
├── marketing/                 # Kickstarter copy, campaign assets, social copy
├── site/                      # Task Force 154 website (HTML/CSS/JS)
├── .gitignore                 # Protects secrets, DS_Store, archives
├── index.html                 # Root web entry point
└── README.md                  # This file
```

---

## Branch Strategy

| Branch | Purpose |
|--------|---------|
| `main` | Stable, production-ready SoT. All validated content lives here. |
| `dev`  | Active working branch. Merge to `main` when ready. |

---

## What Lives Here

- **Task Force 154 website** files (cinematic and standard versions)
- - **Reaper Six** book, cover art, and reader assets
  - - **Brand assets** — favicons, logos, image and document files
    - - **Knowledge base** and editorial materials
      - - **Kickstarter** and marketing copy
       
        - ---

        ## Project Notes

        - Local Claude settings, `.DS_Store` files, secrets, account exports, generated output, and large zip archives are intentionally excluded via `.gitignore`.
        - - Vectored Compliance is excluded — it belongs in its own WTI project lane.
          - - Large binary creative assets are included where they are part of the active TF154 project.
            - - Claude Code is the recommended tool for local commits and pushes from Claude sessions.
             
              - ---

              ## CI / Validation

              A GitHub Actions workflow runs automatically on every push to `main` or `dev`. It checks:
              - All required folders exist (`site`, `brand`, `book`, `audio`, `docs`, `marketing`, `assets`)
              - - Required root files are present (`README.md`, `.gitignore`, `index.html`)
                - - No accidental secret files (`.env`, `.key`) have been committed
                 
                  - ---

                  *Last structural update: May 13, 2026*

---

## Status Log

### 2026-05-14 — SoT Locked / Transitioning to Kickstarter + KDP

**Current state: SoT documentation complete and committed to `main`.**

All 10 core documentation files are in place:

| File | Folder | Status |
|------|--------|--------|
| `series-bible.md` | `book/` | ✅ Committed |
| `characters.md` | `book/` | ✅ Committed |
| `reaper-six-book1-synopsis.md` | `book/` | ✅ Committed |
| `chapter-outline.md` | `book/` | ✅ Committed |
| `lore-and-terminology.md` | `book/` | ✅ Committed |
| `editorial-notes.md` | `docs/` | ✅ Committed |
| `open-threads.md` | `docs/` | ✅ Committed |
| `research-notes.md` | `docs/` | ✅ Committed |
| `kickstarter-copy.md` | `marketing/` | ✅ Committed |
| `taglines.md` | `marketing/` | ✅ Committed |

**Next phase: Kickstarter + KDP**

- Kickstarter campaign build using `marketing/kickstarter-copy.md` as source
- KDP manuscript formatting and upload (Book 1 — *Reaper Six*)
- Campaign assets (cover image, reward tiers, fulfillment logistics) to be added to `marketing/` and `assets/`
- `marketing/kickstarter-copy.md` contains full campaign copy, section structure, tier details, and settings reference

*Last status update: May 14, 2026*
