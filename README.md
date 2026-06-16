# 🧠 Resume Screening with RAG (Retrieval-Augmented Generation)

> An AI-powered resume screening tool that lets recruiters query multiple candidate resumes using natural language — built with ChromaDB, pypdf, and LLaMA 3.3 via Groq.

---

## 🚀 What This Project Does

Tired of manually reading through stacks of resumes? This project automates the screening process by:

- **Ingesting** multiple PDF resumes into a vector database (ChromaDB)
- **Chunking & embedding** resume content for semantic search
- **Answering recruiter queries** like *"Who has experience in Machine Learning?"* using a powerful LLM (LLaMA 3.3 70B via Groq)
- **Comparing candidates** side-by-side based on skills, projects, and certifications

---

## 🛠️ Tech Stack

| Layer | Tool |
|---|---|
| PDF Parsing | `pypdf` |
| Vector Store | `ChromaDB` |
| LLM Backend | `Groq` (LLaMA 3.3 70B Versatile) |
| Runtime | Google Colab / Python 3.12 |

---

## 📁 Project Structure

```
resume-rag/
│
├── resume_screening.ipynb   # Main Colab notebook
├── README.md                # You're here
└── resumes/                 # Upload your PDF resumes here
    ├── candidate1.pdf
    ├── candidate2.pdf
    └── candidate3.pdf
```

---

## ⚙️ How It Works

```
PDF Resumes
    ↓
Extract text (pypdf)
    ↓
Chunk into 1000-char segments
    ↓
Store in ChromaDB vector collection
    ↓
Recruiter asks a question
    ↓
ChromaDB retrieves relevant chunks
    ↓
LLaMA 3.3 (via Groq) generates a structured answer
```

---

## 🧪 Sample Queries You Can Ask

```python
"Who has experience in AI and Machine Learning?"
"Who is skilled in Java programming?"
"Which candidate has the most projects?"
"Who has certifications in cybersecurity?"
"Compare the candidates for a full-stack developer role."
```

---

## 🔧 Setup & Usage

### 1. Clone the repo
```bash
git clone https://github.com/your-username/resume-rag.git
cd resume-rag
```

### 2. Install dependencies
```bash
pip install chromadb pypdf groq
```

### 3. Add your Groq API key
```python
client = Groq(api_key="your_groq_api_key_here")
```
Get a free API key at [console.groq.com](https://console.groq.com)

### 4. Upload resumes & run
Open `resume_screening.ipynb` in Google Colab, upload your PDF resumes when prompted, and run all cells.

---

## 📊 Example Output

**Query:** *"Who has experience in AI and Machine Learning?"*

```
✅ Ramyadevi C — Projects: Spam Email Detection, MedAI
   Certifications: Generative AI (Microsoft), NPTEL Python
   Skills: Scikit-learn, NumPy, Pandas, Flask

✅ Haritha A — Skills: Supervised & Unsupervised Learning,
   Feature Engineering, SVM, Neural Networks, Scikit-learn

✅ Dhanushya R — Projects: PDS Stock Forecasting, AI Chatbot
   Certifications: House Price Prediction (SkillEcted), Power BI
```

---

## 💡 Key Features

- ✅ Supports multiple PDF resumes in one run
- ✅ Semantic search — finds relevant info even without exact keyword matches
- ✅ LLM-generated summaries with candidate comparisons
- ✅ Easily extensible — swap in any LLM or embedding model
- ✅ No database setup needed — ChromaDB runs in-memory

---

## 🔮 Future Improvements

- [ ] Add a web UI with Streamlit or Gradio
- [ ] Support DOCX and plain text resumes
- [ ] Score and rank candidates automatically
- [ ] Export results to CSV/PDF report
- [ ] Add persistent ChromaDB storage

---



Built with ❤️ as a practical AI project exploring RAG pipelines for HR automation.

⭐ **Star this repo if you found it useful!**
