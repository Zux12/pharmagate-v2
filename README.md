# PharmaGATE v2 — Phase 1

Static HTML/CSS/JavaScript pharmacology learning prototype, using a hybrid PharmaGATE and UiTM-inspired visual identity. Not an official UiTM website or clinically validated tool.

## Modules
- Overview and navigation
- Interactive one-compartment IV bolus pharmacokinetics simulator with CSV export
- Illustrative drug comparison (six example drugs)
- Groq AI Tutor (user-supplied temporary test key)

## GitHub Pages deployment
1. Create a GitHub repository (public repository for GitHub Pages on a Free plan).
2. Upload `index.html`, `style.css`, and `app.js` to the repository root.
3. Open repository **Settings → Pages**, select **Deploy from a branch**, choose `main` and `/ (root)`.
4. Open the published URL. No Python, npm, or build process required.

## Groq API
Open Settings in the website, paste a **dedicated testing key**, and enter a model ID supported by your Groq account. The key is held only in JavaScript memory, not stored in the repository or localStorage. Browser requests may fail due to CORS restrictions; if so, a server-side proxy is required. Never commit secrets or use sensitive patient information in this prototype.

## Model and data limitations
The PK simulator assumes a one-compartment instantaneous IV bolus, linear kinetics, and first-order elimination. It is not a dosing calculator. Drug comparison entries are brief illustrative examples and have not undergone a formal source-by-source clinical verification. The Groq tutor may hallucinate. Do not use this application for clinical decisions.

## Future work
Verified drug monographs with per-field references; automated tests; guided experiments and student assessment; persistent accounts and analytics using a backend when needed.
