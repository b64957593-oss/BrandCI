# BrandCI

*Brand governance, as CI/CD.*
Paste marketing content and brand guidelines. AI extracts every claim, matches it to approved facts, scores the risk, and suggests a compliant rewrite. Humans approve at two checkpoints.

*Live demo:* https://b64957593-oss.github.io/BrandCI/

## The problem
Brand and legal teams review content by hand. Risky claims like "removes wrinkles in 3 days" or "number 1 in India" slip through, and expired evidence keeps getting reused. BrandCI works like a CI pipeline: content goes in, a PASS / REVIEW / BLOCK verdict comes out.

## How it works

| Step | What happens | Who |
|---|---|---|
| 01 Input | Paste or upload source content and brand references | You |
| 02 Extraction | Quantitative and important claims are pulled into source.json | Extraction Agent |
| 03 Creator checkpoint | Edit, remove, or add missed claims | Human |
| 04 Reference matching | Each claim is matched to an approved fact and guideline, expired evidence is flagged | Evidence Agent |
| 05 Reviewer checkpoint | Confirm facts, switch off wrong or expired evidence | Human |
| 06 Validate + explain | Every claim is scored Low / Medium / High with the reason and the guideline cited. Tone, language and accessibility issues are also caught | Governance Agents |
| 07 Output | source.json, reference.json, validate.json, suggestions.json | Auto |

The verdict is *BLOCK* if any claim is high risk, *REVIEW* if any is medium, otherwise *PASS*.

## Features
- 3 specialised AI agents with human-in-the-loop checkpoints
- Risk scoring with explanations and cited guidelines
- Suggested compliant rewrites for every flagged claim
- Whole-content checks for tone, language and missing alt text
- Download each JSON file, or everything as one report
- Run history saved in the browser
- Premium dark UI, auto light mode, animated pipeline

## Try it in 1 minute
1. Open the live demo.
2. Go to *Settings, pick **Groq*, and paste a free API key from [console.groq.com](https://console.groq.com).
3. Click *Load sample, then **Extract claims*, and follow the steps.

Your API key is stored only in your own browser and is sent only to the AI provider.

## Tech
- Single-file frontend: HTML, CSS and vanilla JavaScript, no build step
- LLM via any OpenAI-compatible API (Groq or Google Gemini)
- Browser localStorage for settings and run history
- Hosted on GitHub Pages

## Known limits
- The API key lives in the browser, which is fine for a demo but not for production. A production version needs a backend that holds the key.
- Text input only for now (paste, or .txt / .md / .csv / .json).

## Roadmap
- Backend (FastAPI) with a database for shared run history
- Image and PDF extraction with a vision model
- Email and CMS integrations, so BrandCI can gate publishing in a real pipeline
- Per-brand guideline libraries with evidence expiry tracking
