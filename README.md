# GWC SDR Explorer

Interactive dashboard for exploring the Global WASH Cluster Secondary Data Reviews:

- **Area-Based Coordination (ABC)** — barriers and enablers, sources S1–S32  
- **Transition in Humanitarian Settings** — barriers and enablers, sources S1–S34

## Features

- **Findings** — barrier/enabler cards with confidence ratings and takeaways; filter by SDR, type, confidence, country; full-text search; click a card to expand the evidence narrative; click a source chip to jump to its registry entry  
- **Recommendations** — global-level and country-level actions from the NCP Validation Workshop, side by side  
- **Source Registry** — all active (S\#) and archived (A\#) sources with reverse citations ("cited in" shows which findings use each source)  
- **Country View** — pick a country to see every finding that references it, with the relevant evidence highlighted

Everything is a single self-contained `index.html` — no build step, no dependencies, data embedded.

## Publish on GitHub Pages

1. Create a new repository on GitHub (e.g. `gwc-sdr-explorer`), public.  
2. Upload `index.html` and this `README.md` to the repository root (web UI: *Add file → Upload files*).  
3. Go to **Settings → Pages**, under *Build and deployment* set Source \= **Deploy from a branch**, Branch \= **main** / root, and save.  
4. After \~1 minute the dashboard is live at `https://<your-username>.github.io/gwc-sdr-explorer/`.

## Updating the data

The findings, recommendations and registry are embedded as JSON inside `index.html` (search for `const DATA =`). When a new SDR version is finalized, regenerate the JSON from the document text and replace that block — or ask Claude to re-run the extraction.

---

Global WASH Cluster (GWC) · 2026 · Findings traceable to Source IDs in each SDR's Annex 1\.  
