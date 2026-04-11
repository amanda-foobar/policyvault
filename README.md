# PolicyVault

A personal insurance intelligence tool that helps you track, understand, and query all your insurance policies in one place.

> **[→ Open PolicyVault](https://amanda-foobar.github.io/policyvault/)**

Built as a single, self-contained HTML file — no installation, no server, no account required. Just open it in your browser.

---

## What it does

- **Policy management** — add and organise policies across Medical, Travel, Investment / Life, Property, Critical Illness, Motor, Personal Accident, and Domestic Helper categories
- **Document upload** — attach your policy PDFs; the AI reads them and pre-fills policy details automatically
- **AI assistant** — ask natural language questions about your coverage across all policies, with the AI reading your actual documents for precise answers
- **Renewal tracking** — visual expiry warnings, a quick-update flow, and support for uploading renewal notices with AI-assisted extraction
- **Lapsed policy archiving** — expired policies are visually distinguished and retained for reference without cluttering active policies
- **Local-first storage** — all data and documents are stored in your browser's IndexedDB, never sent to any server
- **PIN lock** — optional 4-digit PIN to protect access on shared devices
- **Backup and restore** — export your entire vault (policies + documents) as a single file; reimport on any browser or device

---

## How to use it

1. Click **[Open PolicyVault](https://amanda-foobar.github.io/policyvault/)** above
2. Add your policies manually, or upload a PDF to auto-extract the details
3. Use the AI assistant to ask questions about your coverage

> **Note:** The AI assistant and document extraction features require the Anthropic Claude API, which is currently handled via the Claude.ai infrastructure. For full functionality, open the app through Claude.ai rather than directly from your browser.

---

## Policy types supported

| Type | Icon |
|---|---|
| Critical Illness | 🫀 |
| Domestic Helper | 🏡 |
| Investment / Life | 📈 |
| Medical / Health | 🏥 |
| Motor | 🚗 |
| Personal Accident | 🩹 |
| Property / Home | 🏠 |
| Travel | ✈️ |

---

## Data & privacy

- All policy data and uploaded documents are stored **locally in your browser** using IndexedDB
- Nothing is uploaded to any server or third-party service
- PDFs are only sent to the Anthropic API **in the moment you ask the AI a question** — they are not retained
- Use **Back up data** in the sidebar to export a local copy of your vault at any time

---

## Status

Active personal project — currently single-user, local-only.

**Planned future work:**
- Supabase backend for cloud sync and multi-device access
- Proper multi-user authentication with invite-based onboarding
- Mobile-optimised layout
- Encrypted vault export

---

## Tech

- **Frontend:** Vanilla HTML, CSS, and JavaScript — no frameworks, no build step
- **AI:** Anthropic Claude API (claude-sonnet) for document extraction and the AI assistant
- **Storage:** Browser IndexedDB for policies and documents; localStorage for PIN and display name
- **Fonts:** Lora (headings), DM Sans (body), DM Mono (data)
