# n8n Automation Workflows

Collection of n8n automation workflows using HTTP requests, local LLMs via Ollama, and Google Sheets.

## Workflows

### 🐱 Cat Fact AI Summarizer
Fetches a random cat fact from a public API, processes it with Ollama/Mistral to make it funnier, and saves the result to Google Sheets.

**Nodes used:**
- Manual Trigger
- HTTP Request → `https://catfact.ninja/fact`
- Ollama (Mistral) → makes the fact funnier
- Google Sheets → saves the result

**Import URL:**
https://raw.githubusercontent.com/rohbdn07/n8n-automation/main/cat-fact-ollama-sheets.json

## Requirements
To run these workflows you need:
- [n8n](https://n8n.io) installed (`npm install -g n8n`)
- [Ollama](https://ollama.ai) installed with Mistral pulled (`ollama pull mistral`)
- Google account with Sheets API and Drive API enabled
- Node.js 22 (LTS)

## How to Import
1. Open n8n → `http://localhost:5678`
2. Click `+` to create new workflow
3. Click `...` top right → `Import from URL`
4. Paste the import URL above

## Setup After Import
- Update Ollama credential URL to `http://127.0.0.1:11434`
- Connect your own Google Sheets account
