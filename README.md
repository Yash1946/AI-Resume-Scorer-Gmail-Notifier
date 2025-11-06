# AI-Resume-Scorer-Gmail-Notifier
This project is an **AI-powered Resume Evaluation System** built with **Google Gemini AI** and **Gmail API**, deployed using **Streamlit**.   It analyzes uploaded resumes, generates feedback and a score using Gemini, and can automatically email the feedback to the candidate.  ---
## 🧠 Features

- 📄 **PDF Resume Extraction:** Reads and extracts text from uploaded PDF resumes using `PyMuPDF (fitz)`.
- 🤖 **AI Scoring:** Uses **Google Gemini** to evaluate resumes and provide a score (out of 10) with a short explanation.
- 📧 **Email Automation:** Sends personalized feedback emails automatically using the **Gmail API**.
- 🖥️ **Interactive UI:** Built using **Streamlit** for a clean and easy-to-use interface.

---

## ⚙️ Tech Stack

| Category | Tools / Libraries |
|-----------|------------------|
| 💬 Language | Python |
| 🧠 AI Model | Google Gemini (via `google-generativeai`) |
| 📤 Email API | Gmail API |
| 🖼️ Frontend | Streamlit |
| 📚 PDF Processing | PyMuPDF (`fitz`) |
| 🔐 Auth | OAuth2 (Google Authentication) |

---

## 🏗️ Project Architecture

User Uploads Resume (PDF)
↓
Text Extracted via PyMuPDF
↓
Sent to Gemini Model for Scoring
↓
Feedback + Score Generated
↓
User Can Email Feedback via Gmail API

yaml
Copy code

---

## 🚀 How to Run Locally

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/jayraj-patil/ai-resume-scorer.git
cd ai-resume-scorer
2️⃣ Install Dependencies
bash
Copy code
pip install -r requirements.txt
3️⃣ Setup Google APIs
Create a project in Google Cloud Console

Enable Gmail API

Download credentials.json and place it in your project root

The app will create a token.pkl on first login automatically

4️⃣ Add Gemini API Key
In your Python file (or .env):

python
Copy code
configure(api_key="YOUR_GEMINI_API_KEY")
5️⃣ Run the Streamlit App
bash
Copy code
streamlit run app.py
🧩 Output Preview
User uploads a PDF resume

Gemini gives feedback like:

"Score: 8/10 — Strong technical foundation with clear skills in AI/ML. Add more project details for higher impact."

Optionally sends an email to the candidate with the same feedback
