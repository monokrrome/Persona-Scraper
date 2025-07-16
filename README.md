# 🧠 Persona Scraper

**Persona Scraper** is a Python tool that takes a Reddit username as input, scrapes the user's recent posts and comments, and generates a **detailed user persona** using an LLM (Large Language Model). The generated persona outlines key behavioral and psychological traits such as interests, tone, values, personality, frustrations, goals, and needs — each supported by citations from their Reddit activity.

This project is created as part of the BeyondChats Generative AI Internship assignment.

---

## 🔍 Features

- 🔗 Input: Reddit profile username or URL
- 📄 Scrapes latest posts and comments
- 🤖 Uses OpenChat LLM to analyze user behavior
- 🧑‍💼 Outputs a structured **User Persona**
- 📎 Cites Reddit posts/comments used to derive insights
- 💾 Saves persona as a text file for later use

---

## 📦 Requirements

Install the following Python packages:

```bash
pip install praw transformers accelerate
```

---

# 🛠️ Setup
## **1. Clone this repository:**
```bash
git clone https://github.com/your-username/persona-scraper.git
cd persona-scraper
```

## **2. Add your Reddit API credentials in the script:**
Get credentials from https://www.reddit.com/prefs/apps
Replace these in the code:
```python
reddit = praw.Reddit(
    client_id='YOUR_CLIENT_ID',
    client_secret='YOUR_CLIENT_SECRET',
    user_agent='UserPersonaScraper by /u/YOUR_USERNAME',
    username='YOUR_USERNAME',
    password='YOUR_PASSWORD',
    check_for_async=False
)
```

## **3. Run the script:**
```bash
python persona_scraper.py
```

---

# 📥 Input
In the 'persona_scraper.py', modify the 'username' variable:
```python
username = "kojied"  # Replace with any Reddit username
```

---

# 📤 Output
- A text file named <username>_persona.txt will be created in the same directory.
- Example filename: kojied_persona.txt

# 🧾 Output Format (Example)
```text
User Persona:
- Interests: Technology, Gaming, and Personal Finance [Source: "Post: Title of post..."]
- Tone: Sarcastic and informal [Source: "Comment: ..."]
- Values: Privacy, Community Engagement [Source: ...]
- Personality: Curious, Detail-Oriented [Source: ...]
- Behavior: Frequent commenter, tends to engage in long discussions [Source: ...]
- Frustrations: Moderation policies on subreddits [Source: ...]
- Motivations: Learning and sharing knowledge [Source: ...]
- Goals: Build online presence, stay informed [Source: ...]
- Needs: Access to reliable communities, mental clarity [Source: ...]
```

---

# 📌 Notes
- This tool uses the openchat/openchat-3.5-0106 model from HuggingFace for LLM-based inference.
- Ensure your machine has enough memory (8GB+ RAM recommended). For lower-end systems, try switching to smaller models (e.g., microsoft/phi-2).
- Follow PEP-8 coding guidelines for consistency: https://peps.python.org/pep-0008/

---

# 📁 Project Structure
```bash
persona-scraper/
│
├── persona_scraper.py     # Main script
├── kojied_persona.txt     # Example output
├── Hungry-Move-6603.txt   # Another example output
└── README.md              # This file
```

---

# 💡 Example Usage
To generate persona for user 'Hungry-Move-6603':
```bash
python persona_scraper.py
```
Output: 'Hungry-Move-6603_persona.txt'

---

# 🔐 Disclaimer
This tool is intended for educational and research purposes only. Use responsibly and respect Reddit's API rate limits and privacy guidelines.

---

# 🚀 Author
Built by @monokrrome
