markdown
<h1 align="center">🧠🎙️ Offline Chat Companion</h1>
<p align="center">
A local, privacy-first AI assistant built with LLMs, LangChain, vector memory, and speech processing — all running offline.
</p>

<p align="center">
  <img src="images/offline-companion.gif" alt="Offline Chat Companion Demo" width="600"/>
</p>

---

## 📌 What is this?

The **Offline Chat Companion** is your intelligent, memory-enhanced chat assistant designed to work completely offline — no internet, no cloud, just you and your device. It's perfect for:

- 🔒 Privacy advocates  
- 💻 Developers seeking a customizable AI chatbot  
- 🧠 Experiments with memory-enhanced LLMs  
- 🎙️ Speech-based offline assistants  

---

## ✨ Features

- 🧠 **Local LLM Integration**: Built on **Alpaca.cpp** using **Dalai** for local inference  
- 💬 **Natural Language Chat Interface**: Type or speak your inputs  
- 🗣️ **Speech-to-Text + Text-to-Speech**: Full voice interaction using offline STT and TTS  
- 🧬 **Memory Module**: FAISS-powered vector database stores past interactions  
- 🔗 **LangChain Integration**: Tool chaining and custom agents  
- 🚫 **100% Offline**: Works without internet — your data stays on your machine  

---

## 🎥 Screenshots & Demo

### 🧠 Chat Companion in Action
<p align="center">
  <img src="images/offline_.png" alt="Offline Chat UI" width="500"/>
</p>

### 🎞️ Demo GIF
<p align="center">
  <img src="images/offline-companion.gif" alt="Chat Companion Demo" width="600"/>
</p>

---

## 🧬 How It Works

The **Offline Chat Companion** runs entirely offline using open-source technologies and your machine's hardware.

### 📂 1. Model Setup & Hosting
- `npx dalai serve` spins up a local server and loads Alpaca 7B.  
- All model files are stored locally; no further internet needed.

### 💬 2. Chat Interface
- HTML + JS frontend served at `http://localhost:3000`  
- Input text is sent to Dalai via HTTP

### 🧠 3. Inference Pipeline
```text
User Prompt → Dalai Server → Alpaca Model → Generated Response → Sent Back to UI
```

### ⚙️ 4. Parameter Controls
- Customize temperature, top_k, n_predict, repeat_penalty to shape response style

### 🔐 5. Offline by Design
- Zero API keys or cloud dependencies  
- Ideal for private setups or air-gapped systems

---

## 🛠 Tech Stack

| Tool / Library        | Purpose                         |
|----------------------|---------------------------------|
| `Dalai`              | Serve LLaMA / Alpaca locally     |
| `Alpaca.cpp`         | Lightweight LLM backend          |
| `LangChain`          | Agent framework / memory tools   |
| `FAISS`              | Vector search DB (for memory)    |
| `Whisper` (Offline)  | Speech-to-text                   |
| `Coqui TTS` / `pyttsx3` | Text-to-speech engine        |
| `Gradio` / `Tkinter` | (Optional) for GUI frontend      |

---

## 🗂️ Project Structure

```bash
offline-chat-companion/
├── app.py                    # Main script to run the companion
├── llama_interface.py        # Handles LLM interaction
├── langchain_interface.py    # LangChain integration and chaining
├── memory/
│   ├── vector_db/            # FAISS-based memory storage
│   └── memory_utils.py
├── speech/
│   ├── stt.py                # Speech-to-text module
│   └── tts.py                # Text-to-speech module
├── images/                   # Screenshots & GIFs
├── requirements.txt
└── README.md
```

---

## 🚀 Getting Started

### 📥 Clone & Install

```bash
git clone https://github.com/nyhereo-benzai1/offline-chat-companion.git
cd offline-chat-companion
pip install -r requirements.txt
```

### ▶️ Run the App

```bash
python app.py
```

Make sure you have a local LLaMA or Alpaca model installed via [Dalai](https://github.com/cocktailpeanut/dalai).

---

## 🛤️ Roadmap

- ✅ Initial local LLM integration  
- ✅ STT + TTS support (voice interaction)  
- ✅ Memory module with FAISS  
- 🔲 Add personality presets / modes  
- 🔲 GUI frontend (Tkinter or Gradio)  
- 🔲 Multilingual support  
- 🔲 Agent-based actions (file search, note writing, etc.)  

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you’d like to change.

---

## 💖 Made with Love by Nyx

> *“Building my own AI, one offline neuron at a time.”*

<p align="center">
  <img src="https://img.shields.io/github/stars/nyhereo-benzai1/offline-chat-companion?style=social">
  <img src="https://img.shields.io/github/forks/nyhereo-benzai1/offline-chat-companion?style=social">
</p>
```

---

Just go to your repo > click on `README.md` > click the ✏️ pencil icon to edit, and paste this content in. Let me know when you're ready for the GitHub profile README magic! 🌟
