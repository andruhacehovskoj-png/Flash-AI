# ⚡ Flash AI

> Desktop AI chat application powered by OpenRouter. Fast, beautiful, multilingual.

![Python](https://img.shields.io/badge/Python-3.12-blue)
![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey)
![License](https://img.shields.io/badge/License-MIT-green)

## ✨ Features

- 🔐 **GitHub OAuth login** — no passwords, no signup forms
- 🌍 **Multi-language UI** — English, Русский, Español, Français, Українська
- 💬 **Chat history** — saved to disk, grouped by date (Today / Yesterday / 7 days / 30 days)
- 🎨 **Beautiful interface** — dark theme, smooth animations, rounded message bubbles
- ⚡ **Streaming responses** — typewriter effect for AI answers
- 📝 **Markdown + code highlighting** — supports Python, JavaScript, C++, Lua, and 190+ more languages
- 📋 **Copy & download** — one-click copy or save any code block
- 🖥️ **Native window** — powered by pywebview, no browser needed
- 📦 **Single .exe** — ready-to-run build, no Python installation required

## 🖼️ Screenshots

_(add screenshots here later)_

## 🚀 Quick Start

### Option 1: Download the .exe

Grab the latest `FlashAI.exe` from the [Releases](../../releases) page and run it. No installation needed.

### Option 2: Run from source

```bash
git clone https://github.com/YOUR_USERNAME/flashai-desktop.git
cd flashai-desktop
pip install -r requirements.txt
python flash_ai.py
```

## ⚙️ Configuration

1. Get a free API key at [openrouter.ai/keys](https://openrouter.ai/keys)
2. Open `flash_ai.py` and set your key:
   ```python
   OPENROUTER_API_KEY = "sk-or-v1-..."
   ```
3. Run the app — first time it will ask you to sign in with GitHub

## 🏗️ Build from Source

Requires **Python 3.12** (PyInstaller doesn't support 3.14 yet).

```bash
pip install pyinstaller pywebview openai requests pillow
pyinstaller --noconfirm --onefile --windowed --name "FlashAI" --icon="flash_ai.ico" --add-data "flash_ai.png;." flash_ai.py
```

The output `.exe` will be in the `dist/` folder.

## 🧱 Tech Stack

| Component | Technology |
|-----------|------------|
| Backend   | Python 3.12, `http.server` |
| GUI       | pywebview + HTML/CSS/JS |
| AI        | OpenRouter API |
| Auth      | GitHub OAuth Device Flow |
| Syntax    | highlight.js |
| Storage   | JSON files in user home directory |

## 📁 Project Structure

```
flashai-desktop/
├── flash_ai.py          # Main application
├── flash_ai.png         # App icon
├── flash_ai.ico         # Windows icon
├── requirements.txt     # Python dependencies
├── README.md            # This file
├── LICENSE              # MIT
└── .gitignore
```

## 🔒 Privacy

- **No data leaves your machine** except API requests to OpenRouter
- Chats are stored locally in `~/.flashai_chats.json`
- Settings are stored locally in `~/.flashai_settings.json`
- GitHub token is stored locally in `~/.flashai_token`
- **You can log out anytime** — clears the local token

## 🌐 Supported Languages

| Code | Language |
|------|----------|
| `en` | English |
| `ru` | Русский |
| `es` | Español |
| `fr` | Français |
| `uk` | Українська |

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first.

## 📜 License

MIT — see [LICENSE](LICENSE) for details.

## ⚠️ Important

Never commit your API key. If you accidentally do — **revoke it immediately** at [openrouter.ai/keys](https://openrouter.ai/keys).

## 🙏 Credits

- [OpenRouter](https://openrouter.ai) — AI API
- [pywebview](https://pywebview.flowrl.com/) — native window wrapper
- [highlight.js](https://highlightjs.org/) — syntax highlighting

---

Made with ⚡ by [@YOUR_USERNAME](https://github.com/YOUR_USERNAME)
