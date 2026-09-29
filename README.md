# 💬 ResponseCraft

**Paste a message. Choose the tone. Get a ready-to-send reply.**

ResponseCraft is a small AI web app that writes replies for WhatsApp, LinkedIn, Email, Instagram, Slack and Twitter / X. Tell it who you are replying to and how you feel, then copy the result with one click.

add-pink-theme
<!-- 🔗 **Live app:** _add your Streamlit link here_ -->
<!-- 🔗 **Live app:** https://responsecraft-ai-studio.streamlit.app/ -->
< main -->

---

## ✨ What it does

- Writes in the right style for each **platform** (casual on WhatsApp, polished on LinkedIn)
- Adapts to the **person**: friend, partner, family, manager, client and more
- **11 tones**: professional, sweet, flirty, apologetic, firm, busy and others
- **Short, Medium or Detailed** replies
- Works in **English, Hindi or Hinglish**
- **Quick situations**: Polite no, Late reply, Follow-up and more, in one click
- Gives **1 to 3 options** and a **Copy** button for each

---

## 🚀 Quick Start

You need Python 3.10+ and a free [Groq API key](https://console.groq.com).

```bash
# 1. Get the code
git clone https://github.com/YOUR_USERNAME/responsecraft.git
cd responsecraft

# 2. Install
pip install -r requirements.txt

# 3. Run
streamlit run app.py
```

Before running, create the file `.streamlit/secrets.toml` and add your key:

```toml
GROQ_API_KEY = "your_key_here"
```

The app opens at http://localhost:8501

---

## ☁️ Deploy (free)

1. Push the project to GitHub.
2. Open [share.streamlit.io](https://share.streamlit.io) and click **Create app**.
3. Pick your repo, branch `main`, file `app.py`.
4. In **Advanced settings → Secrets**, paste `GROQ_API_KEY = "your_key_here"`.
5. Click **Deploy**.

Every push to GitHub updates the live app automatically.

---

## 🛠 Customise

| I want to... | Change this |
| --- | --- |
| Change colours | Colour list at the top of `app.py`, and `.streamlit/config.toml` |
| Add a quick situation | `PRESETS` in `app.py` |
| Change the reply limit | `MAX_REQUESTS_PER_HOUR` in `app.py` |
| Use a different AI model | Add `GROQ_MODEL = "model-name"` in Secrets |

---

## 📁 Files

```
app.py                   the app
requirements.txt         packages to install
.streamlit/config.toml   theme (black and green)
.streamlit/secrets.toml  your API key (never uploaded)
```

---

## 🔒 Keep your key safe

- Never upload `secrets.toml` to GitHub. The `.gitignore` file already blocks it.
- If your key is ever exposed, delete it in the Groq console and make a new one.

---

## 🗺 Coming next

- Reply history
- Pink and white theme
- Voice input

---

## 👤 Author
 add-pink-theme
Made by **Yash**. If this helps you, give it a ⭐

Made by **Yash**. 
If this helps you, give it a ⭐
main
