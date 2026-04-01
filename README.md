# 🚀 AI Career Coach – Resume Analyser
An AI-powered web application that analyzes resumes for **ATS compatibility**, detects **skill gaps**, matches profiles to **job roles**, and generates a **professional downloadable report**.

---

## ✨ Features

* 📄 Upload resumes (**PDF, DOCX, TXT**)
* 🧠 AI-powered analysis using **Gemini API**
* 📊 ATS Score with detailed breakdown
* 🎯 Job role matching system
* 🔍 Skills detection (present vs missing)
* ✏️ Actionable improvement suggestions
* ✨ **AI Resume Improvement** (auto-generates a refined version of resume)
* 📊 **Score Comparison History** (track improvement between multiple analyses)
* 📥 Download full analysis as a **PDF report**
* ⚡ Clean, responsive UI (mobile + desktop optimized)

---

## 🛠 Tech Stack

* **Frontend:** React (Vite)
* **Backend:** Node.js, Express
* **AI:** Gemini API
* **Libraries:**

  * `pdfjs-dist` → PDF parsing
  * `mammoth` → DOCX parsing
  * `jspdf` → PDF report generation

---

## 📂 Project Structure

```
smart-resume-analyser/
│
├── public/
├── src/
│   ├── assets/
│   ├── App.jsx        # Core UI + logic + AI features
│   ├── App.css
│   ├── index.css
│   └── main.jsx
│
├── proxy.cjs          # Backend (Gemini API handler)
├── package.json
├── vite.config.js
└── README.md
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/ai-career-coach.git
cd ai-career-coach
```

---

### 2️⃣ Install Dependencies

```bash
npm install
```

---

## ▶️ Run Frontend

```bash
npm run dev
```

App runs at:

```
http://localhost:5173
```

---

## 🔌 Backend Setup (Required)

Frontend sends requests to:

```
http://localhost:3001/api/analyse
```

So backend must be running.

---

### 1️⃣ Install Backend Dependencies

```bash
npm install express cors dotenv node-fetch
```

---

### 2️⃣ Create `.env` file

```env
GEMINI_API_KEY=your_api_key_here
```

---

### 3️⃣ Start Backend Server

```bash
node proxy.cjs
```

---

## 🧠 How It Works

1. User uploads resume
2. Resume is parsed:

   * PDF → `pdfjs-dist`
   * DOCX → `mammoth`
   * TXT → FileReader
3. Content is processed and optimized
4. AI prompt is generated dynamically
5. Request sent to backend proxy
6. Gemini API analyzes resume
7. Structured JSON response returned
8. UI displays:

   * ATS Score
   * Skills & gaps
   * Improvements
   * Job match
9. User can:

   * Improve resume using AI
   * Compare scores with previous attempts
   * Download a **PDF report**

---

## 📥 PDF Report

Generated report includes:

* ATS Score + breakdown
* Job match analysis
* Skills & missing skills
* Improvement suggestions
* Final professional evaluation

Saved as:

```
resume-report.pdf
```

---

## ⚠️ Notes

* Backend server must be running before analysis
* Gemini API key is required
* Large resumes are trimmed for performance

---

## 🔮 Future Improvements

* Resume rewriting enhancements
* Advanced comparison analytics
* Cloud deployment (Vercel + Render)
* User authentication
* Saved report history

---

## 👩‍💻 Author

**Nimmi**
Built with focus on real-world product design, AI integration, and user experience.
