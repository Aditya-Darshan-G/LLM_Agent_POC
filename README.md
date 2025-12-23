Deployed on Hugging Face at https://huggingface.co/spaces/Aditya-Darshan-G/LLM-Agent-POC

# Browser LLM Agent (AI Pipe) — Multi-Tool POC

A minimal, hackable **browser-only** agent using **OpenAI-style tool calls** with **AI Pipe** (no backend).
It can search the web, run quick LLM transforms (summarize/extract/outline), and execute JavaScript in a sandbox.

---

## Features

- **Provider:** AI Pipe (OpenAI-compatible)
- **Tools:**
  - `google_search(query, limit)` → Google CSE or DDG+Wikipedia fallback  
  - `ai_pipe(workflow, data)` → custom workflow URL or AI Pipe Responses  
  - `execute_javascript(code)` → sandboxed iframe; returns logs + result
- **Design:** small codebase, clear UI, solid error alerts, easy to extend

---

## Quick Start

1. **Get an AI Pipe token**  
   Visit [aipipe.org/login](https://aipipe.org/login) and sign in with Google.

2. **Run this Space**  
   - Enter your token + model (e.g., `gpt-4.1-nano`) in the config panel  
   - Optional: add Google CSE ID + API key for higher-quality search  

3. **Try it out**  
   - `Search IBM annual revenue 2023 site:ibm.com`  
   - `Summarize with AI Pipe: <paste paragraphs>`  
   - `Run JS: console.log("hi"); return 21*2;`

---

## Notes

- All logic runs **in the browser** — no backend required.  
- Do **not** hardcode your AI Pipe token; paste it in at runtime.  
- GitHub Pages or Hugging Face Spaces can both host this as a static site.  

---

## Credits

- [AI Pipe](https://aipipe.org/) by Prof. S. Anand  
- Google CSE, DuckDuckGo, Wikipedia APIs
