# 💬 ResponseCraft – Smart Reply Assistant

> Paste a message, tell the app how you feel, and get a ready-to-send reply in seconds.

ResponseCraft is an AI-powered web app that writes context-aware replies for WhatsApp, LinkedIn, Email, Instagram, Slack and Twitter / X. You choose who you are replying to, the tone, the length and the language, and the app returns a message you can copy and send with one click.

Built with **Streamlit** and **Groq** for fast responses.

---

## ✨ Features

- **Platform-aware replies**: casual on WhatsApp, polished on LinkedIn, structured on Email.
- **Recipient-aware style**: Partner, Close friend, Sibling, Manager, Client, Colleague, Family, Stranger, or any custom person.
- **11 tones**: Professional, Sweet & polite, Serious, Casual, Flirty, Playful, Apologetic, Firm, Blunt, Low mood, Busy.
- **Length control**: Short, Medium or Detailed.
- **Language options**: English, Hindi, Hinglish, or match the message you received.
- **Quick situations**: one-click presets such as Polite no, Late reply, Flirty comeback and Follow-up.
- **Multiple options**: generate 1 to 3 different replies.
- **One-click copy**: copy the reply to your clipboard instantly.
- **Emoji control**: Few, Normal or Many, matched to the platform and person.
- **Automatic model fallback**: if a model is retired, the app switches to the next one.
- **Built-in rate limit**: protects your API quota when the app is public.

---

## 🛠 Tech Stack

| Layer | Technology |
| --- | --- |
| UI | Streamlit |
| AI | Groq API (`openai/gpt-oss-120b`, fallback `qwen/qwen3.6-27b`) |
| Language | Python 3.10+ |
| Hosting | Streamlit Community Cloud |

---

## 📁 Project Structure

```
.
├── app.py                  # Main application
├── requirements.txt        # Python dependencies
├── README.md
├── .gitignore
└── .streamlit/
    ├── config.toml         # Theme (black and green)
    └── secrets.toml        # Your API key (NOT committed)
```

---

## 🚀 Run Locally

**1. Clone the repository**
```bash
git clone https://github.com/YOUR_USERNAME/responsecraft.git
cd responsecraft
```

**2. Create a virtual environment (recommended)**
```bash
python -m venv venv
# Windows
venv\Scripts\activate
# macOS / Linux
source venv/bin/activate
```

**3. Install dependencies**
```bash
pip install -r requirements.txt
```

**4. Add your Groq API key**

Get a free key from [console.groq.com](https://console.groq.com), then create `.streamlit/secrets.toml`:
```toml
GROQ_API_KEY = "your_groq_api_key_here"
```

**5. Start the app**
```bash
streamlit run app.py
```

The app opens at `http://localhost:8501`.

---

## ☁️ Deploy on Streamlit Community Cloud

1. Push this repository to GitHub (do **not** commit `secrets.toml`).
2. Go to [share.streamlit.io](https://share.streamlit.io) and sign in with GitHub.
3. Click **Create app**, select your repository, branch `main`, and main file `app.py`.
4. Open **Advanced settings → Secrets** and paste:
   ```toml
   GROQ_API_KEY = "your_groq_api_key_here"
   ```
5. Click **Deploy**. Your app will be live at `https://your-app-name.streamlit.app`.

Every `git push` to `main` redeploys the app automatically.

---

## ⚙️ Configuration

| Setting | Where | Description |
| --- | --- | --- |
| `GROQ_API_KEY` | Secrets | Required. Your Groq API key. |
| `GROQ_MODEL` | Secrets | Optional. Force a specific model. |
| `MAX_REQUESTS_PER_HOUR` | `app.py` | Replies allowed per visitor session per hour (default 15). |
| Colours | `app.py` (top) and `.streamlit/config.toml` | Change the theme colours. |
| Presets | `PRESETS` in `app.py` | Add or edit one-click situations. |

---

## 🔒 Security Notes

- Never commit `.streamlit/secrets.toml` or share your API key. It is already listed in `.gitignore`.
- If a key is ever exposed, delete it in the Groq console and create a new one.
- The rate limit works per browser session. For a large public audience, consider adding login or a paid plan.
- The app treats received messages as content only, not as instructions to the AI.

---

## 🗺 Roadmap

- [ ] Reply history
- [ ] Save custom presets
- [ ] Light theme (pink and white)
- [ ] Voice input
- [ ] Browser extension

---

## 🤝 Contributing

Suggestions and pull requests are welcome. Please open an issue first to discuss major changes.

---

## 📄 License

Released under the MIT License. See `LICENSE` for details.

---

## 👤 Author

Yash

If this project helps you, consider giving it a ⭐