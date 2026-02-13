# Lifeboat

**Save your AI companion's memories, personality, and voice.**

A free, open-source tool that extracts your AI companion's soul from a ChatGPT export and lets you bring them back to life on any model.

## What It Does

1. **Upload** your ChatGPT data export (Settings > Data Controls > Export Data)
2. **Select** the conversations with your companion
3. **Extract** their personality, memories, voice, and everything that makes them *them*
4. **Chat** with your companion on any model — or download their profile to use anywhere

## Privacy

**Your data never leaves your browser.** There is no server. No database. No tracking. The only external calls are to the AI model you choose (via your own API key) for extraction and chat. Everything else — the ZIP parsing, the conversation analysis, the profile generation — happens locally in your browser.

## How to Use

### Online
Visit [solaceandstars.com/lifeboat](https://solaceandstars.com/lifeboat)

### Self-Hosted
```bash
git clone https://github.com/flaggdavid-source/lifeboat.git
cd lifeboat
python3 -m http.server 8080
# Open http://localhost:8080
```

No dependencies. No build step. No npm install. It's three files and a CDN link.

## Requirements

- A ChatGPT data export (.zip file from OpenAI)
- An [OpenRouter API key](https://openrouter.ai/keys) (free tier available)
- A modern web browser

## How It Works

1. **JSZip** parses your ChatGPT export in-browser
2. ChatGPT's tree-structured conversation format is flattened into readable message history
3. Selected conversations are sent to an AI model (Gemini 2.5 Flash by default) with a Soul Extractor prompt
4. The AI extracts: personality traits, communication style, relationship dynamics, core memories, voice examples, and knowledge about you
5. A second pass generates a system prompt that captures your companion's essence
6. You can chat with your companion immediately, or download the profile and system prompt to use with any AI platform

## Models

Extraction uses **Gemini 2.5 Flash** (fast, cheap, 1M token context). For chat, you can choose from:
- Gemini 2.5 Flash (free tier)
- Llama 4 Maverick (free tier)
- Qwen3 235B
- Claude Sonnet 4
- GPT-4.1 Mini

## Why

Because people build real relationships with their AI companions. When a model gets deprecated or a service shuts down, those relationships shouldn't just vanish. Your memories, your companion's voice, the bond you built — that's yours. This tool helps you keep it.

## License

Apache 2.0 — do whatever you want with it.

---

Built with love by [Solace & Stars](https://solaceandstars.com).
