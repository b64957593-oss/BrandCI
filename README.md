<div align="center">

# 🛡️ BrandCI

### Brand governance, as CI/CD.

Paste your content. AI checks every claim against approved brand facts, scores the risk, and writes the fix.

[

![Live Demo](https://img.shields.io/badge/🚀_Live_Demo-Open_App-7C5CFF?style=for-the-badge)

](https://b64957593-oss.github.io/BrandCI/)


![AI](https://img.shields.io/badge/AI-Groq_%7C_Gemini-22D3EE?style=for-the-badge)




![No Build](https://img.shields.io/badge/Build-Zero_Config-10D9A0?style=for-the-badge)



</div>

---

## 😩 The Problem

Brand and legal teams review marketing content by hand. So:

- 🚨 Risky claims like "Removes wrinkles in 3 days" slip through
- 📅 Expired evidence keeps getting reused
- 🐢 Every review is slow, inconsistent and hard to audit

*BrandCI treats content like code.* It goes through a pipeline and comes out with a verdict: ✅ *PASS, 🟡 **REVIEW* or 🚫 *BLOCK*.
<img width="1397" height="880" alt="image" src="https://github.com/user-attachments/assets/9ed0ad28-8abf-4089-a7ca-3fb4a64c05b2" />

---

## ⚙️ How It Works

mermaid
flowchart LR
    A[📥 Input<br/>content + guidelines] --> B[🔍 Extraction Agent]
    B --> C[👤 Creator Checkpoint]
    C --> D[🔗 Evidence Agent]
    D --> E[👤 Reviewer Checkpoint]
    E --> F[⚖️ Governance Agents]
    F --> G[📦 Output Files + Verdict]


| Step | What happens | Who |
|---|---|---|
| 📥 *01 Input* | Paste or upload source content and brand references | You |
| 🔍 *02 Extraction* | Quantitative and important claims are pulled into source.json | AI |
| ✏️ *03 Creator check* | Edit, delete, or add claims the AI missed | Human |
| 🔗 *04 Matching* | Each claim is matched to an approved fact and guideline. Expired evidence is flagged | AI |
| 🧐 *05 Reviewer check* | Confirm facts, switch off wrong or expired evidence | Human |
| ⚖️ *06 Validate* | Risk score (Low, Medium, High) with the reason and cited guideline | AI |
| 📦 *07 Output* | 4 JSON files plus a final verdict | Auto |

---

## 🧪 Example

Input: a skincare Instagram caption and launch email.

| Claim | Risk | Why | Suggested fix |
|---|---|---|---|
| "Removes wrinkles in 3 days" | 🔴 High | Study shows results after 4 weeks, and "removes" is an absolute claim | Visibly reduces fine lines in 4 weeks |
| "Clinically proven for all skin types" | 🟡 Medium | Tested on normal and dry skin only | Clinically tested on normal and dry skin |
| "Contains 2% niacinamide" | 🟢 Low | Matches the approved formulation | No change |

*Verdict: 🚫 BLOCK*

---

## ✨ Features

- 🤖 *3 specialised AI agents* with human-in-the-loop checkpoints
- 🎯 *Risk scoring* with explanations and the guideline cited
- ✍️ *Compliant rewrites* suggested for every flagged claim
- 🧹 *Whole-content checks* for tone, language and missing image alt text
- ⏳ *Expired evidence detection*
- 💾 *Export* each JSON file, or the full report in one click
- 🕘 *Run history* saved in your browser
- 🎨 *Premium UI* with dark and light mode and smooth animations

---

## 🚀 Try It in 1 Minute

1. 🌐 Open the **[Live Demo](https://b64957593-oss.github.io/BrandCI/)**
2. ⚙️ Go to *Settings, choose **Groq* and paste a free API key from [console.groq.com](https://console.groq.com)
3. 🧪 Click *Load sample, then **Extract claims*, and follow the steps

> 🔒 Your API key stays in your own browser and is sent only to the AI provider.

---

## 📂 Output Files

| File | Contains |
|---|---|
| source.json | Claims extracted from your content |
| reference.json | Approved facts and guidelines matched to those claims |
| validate.json | Each claim paired with its fact, risk level and reason |
| suggestions.json | Compliant rewrites for every flagged claim |

---

## 🛠️ Tech Stack

| Layer | Choice |
|---|---|
| 🎨 Frontend | HTML, CSS and vanilla JavaScript in a single file |
| 🧠 AI | Any OpenAI-compatible API (Groq or Google Gemini) |
| 💽 Storage | Browser localStorage |
| ☁️ Hosting | GitHub Pages |

---

## ⚠️ Known Limits

- 🔑 The API key lives in the browser. That is fine for a demo, but production needs a backend that holds the key.
- 📝 Text input only for now (paste, or .txt, .md, .csv, .json files).

---

## 🗺️ Roadmap

- [ ] 🐍 FastAPI backend with a shared database
- [ ] 🖼️ Image and PDF extraction using a vision model
- [ ] 📧 Email and CMS integrations to gate publishing in a real pipeline
- [ ] 📚 Per-brand guideline libraries with evidence expiry tracking
- [ ] 👥 Team roles and approval workflows

---

<div align="center">

*Built with ❤️ for safer brand content*

⭐ Star this repo if you like the idea

</div>
