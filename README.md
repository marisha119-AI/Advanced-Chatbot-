# 🤖 Advanced Chatbot — Enterprise AI Console

A high-performance, enterprise-grade AI chatbot built with pure HTML/CSS/JavaScript,
powered by OpenRouter's free LLM models and secured via Cloudflare Workers.
---

## ✨ Features

- 🤖 **Multi-model support** — Arcee Trinity, Mistral 7B, DeepSeek R1, LLaMA 3.2, Gemma, Qwen3
- 🔊 **Voice output** — AI responses read aloud with speed & pitch controls
- 📋 **Copy button** — one-click copy on every AI response
- 🌐 **Multilingual** — responds fluently in any language
- ⚡ **Quick Prompts** — built-in business prompt shortcuts
- 📊 **Session stats** — message count, model name, token tracker
- 🔐 **Secure** — API key hidden via Cloudflare Worker proxy

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML / CSS / JavaScript | Frontend UI |
| OpenRouter API | LLM model access |
| Cloudflare Workers | Secure API proxy (hides API key) |
| GitHub Pages | Free hosting |
| Web Speech API | Voice output |

---

## 🔐 Security

This project uses **Cloudflare Workers** as a secure proxy.  
The OpenRouter API key is stored as an **encrypted environment variable** inside Cloudflare — it is never exposed in the frontend code or GitHub repository.

---

## 🚀 How to Deploy Your Own

### Step 1 — Cloudflare Worker
1. Go to [cloudflare.com](https://cloudflare.com) → Workers & Pages → Create Worker
2. Paste the `worker.js` code
3. Go to Settings → Variables and Secrets → Add Secret:
   - Name: `OPENROUTER_API_KEY`
   - Value: your key from [openrouter.ai/keys](https://openrouter.ai/keys)
4. Deploy

### Step 2 — Update index.html
```js
const PROXY_URL = "https://your-worker.your-name.workers.dev";
```

### Step 3 — Deploy to GitHub Pages
1. Push `index.html` to GitHub
2. Go to repo Settings → Pages → Deploy from main branch
3. Your chatbot is live! 🎉

---

## 📁 Project Structure
```
advanced-chatbot/
├── index.html      ← Complete frontend (no API key)
├── worker.js       ← Cloudflare Worker proxy code
└── README.md       ← This file
```

---

## 👩‍💻 About

Built by **Marisha Dwivedi** — AI  Intern | AI Enthusiast  
Currently seeking remote AI roles: Prompt Engineer · AI Trainer · LLM Evaluator

