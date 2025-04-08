
# 🧠 Offline Chat Companion

An **offline AI chatbot** powered by open-source LLMs (like Alpaca 7B) using [Dalai](https://github.com/cocktailpeanut/dalai). This project allows you to run a lightweight version of ChatGPT **completely on your local machine** without requiring internet or API keys.

---

## 🚀 Features

- 💻 **Runs fully offline** – No OpenAI keys or internet needed
- 🧠 **Powered by LLaMA / Alpaca** – Open-source large language models
- 🌐 **Local Web Interface** – Chat through a browser UI
- 🧩 **Simple Setup** – Start with just a few commands

---

## 📸 Screenshot

![screenshot](https://github.com/nyhereo-benzai1/offline-chat-companion/assets/preview.png)  
*Your AI companion running locally.*

---

## ⚙️ Tech Stack

- 🧠 **LLM**: Alpaca 7B (via Dalai)
- ⚙️ **Runtime**: Node.js, npm
- 🌐 **Frontend**: HTML, JavaScript
- 🧰 **Backend (via Dalai)**: Node server serving the local model

---

## 🛠️ Installation Guide

### 1. Clone the Repo
```bash
git clone https://github.com/nyhereo-benzai1/offline-chat-companion.git
cd offline-chat-companion
```

### 2. Install Dalai
```bash
npx dalai install
```

> This will download the Alpaca model and set it up.

### 3. Run the Local Server
```bash
npx dalai serve
```

Now, open your browser and go to [http://localhost:3000](http://localhost:3000) to start chatting.

---

## 🗃️ Folder Structure

```
offline-chat-companion/
├── dalai/                # Auto-generated model & server
├── client/               # Frontend UI (optional customization)
├── package.json          # Node project config
├── README.md             # You are here!
└── ...
```

---

## 🧠 How It Works (Detailed)

This project uses **Dalai** to run an open-source language model locally (like Alpaca 7B), which you can chat with through a web interface.

### 1. Dalai Framework (Backend)
Dalai is a Node.js-based tool that:
- Downloads and prepares LLaMA-based models
- Starts a **local server** at `http://localhost:3000`
- Handles the **prompt-to-response pipeline**

It manages:
- Tokenization and detokenization
- Formatting input prompts
- Streaming back model-generated responses

### 2. Local LLM: Alpaca 7B
Alpaca is a fine-tuned version of Meta’s LLaMA model designed for instruction-following. Once installed:
```bash
npx dalai alpaca install 7B
```
you can run it fully offline.

The model:
- Takes in a prompt like:  
  _"Instruction: Explain black holes. Input: [user message]"_
- Returns a thoughtful response generated in real-time

### 3. Frontend UI
- Your browser sends the user input to the Dalai server
- The server uses Alpaca to process it
- The output is sent back and displayed in a chat-like interface

### 4. End-to-End Flow

```text
User Input  →  Browser UI  →  Dalai Server  →  Alpaca 7B Model
                                ↓
                           Generated Text
                                ↓
                        Sent back to UI
```

---

## ❓ FAQ

**Q: Is this really offline?**  
Yes! Once installed, the chatbot runs entirely on your system. No cloud or external calls are made.

**Q: How is this different from ChatGPT?**  
It uses Alpaca, an open-source alternative fine-tuned for instruction following, rather than OpenAI's proprietary models.

**Q: Can I use other models?**  
Dalai also supports LLaMA 7B/13B and Alpaca 13B if your hardware allows it.

---

## 🔮 Future Plans

- 🧠 Add memory (store previous chats)
- 🎤 Add voice input/output using TTS + STT
- 🧪 Add search/knowledge tools via local vector DBs
- 🧠 Switch backend to Python (Flask) for extension flexibility
- 📲 Package as a desktop/mobile app

---

## 🙋‍♀️ About Me

Made with 💙 by **Nyx** – An aspiring AI developer & innovator.  
🔗 [github.com/nyhereo-benzai1](https://github.com/nyhereo-benzai1)

---

## 📄 License

This project is for educational and personal use only.  
Please follow original model authors’ licenses (e.g., Alpaca, LLaMA, Dalai).
