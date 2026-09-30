# LegalEase - AI-Powered Legal Document Generator & Simplifier

> Bridging the gap between complex legal language and common people through AI + Tanglish.

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue)](https://python.org)
[![FastAPI](https://img.shields.io/badge/Backend-FastAPI-green)](https://fastapi.tiangolo.com/)
[![Gemini](https://img.shields.io/badge/AI-Google%20Gemini%201.5%20Pro-orange)](https://ai.google.dev/)
[![License](https://img.shields.io/badge/License-MIT-yellow)](LICENSE)

### 🔗 Live Project Link: [Will be deployed soon]
### 📂 GitHub Repository: Public

---

## 📌 Problem Statement

In India, 90% of people sign legal documents (Rent Agreement, Job Contracts, NDA) without understanding the terms because they are written in complex English legal jargon. This leads to exploitation, especially in Tamil Nadu where English is not primary. There is no affordable tool that generates legally sound documents AND explains them in local Tanglish.

---


LegalEase - AI-Powered Legal Document Generator & Simplifier

> Bridging the gap between complex legal language and common people through AI + Tanglish.

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue)](https://python.org)
[![FastAPI](https://img.shields.io/badge/Backend-FastAPI-green)](https://fastapi.tiangolo.com/)
[![Gemini](https://img.shields.io/badge/AI-Google%20Gemini%201.5%20Pro-orange)](https://ai.google.dev/)
[![License](https://img.shields.io/badge/License-MIT-yellow)](LICENSE)

🔗 Live Project Link: [Will be deployed soon]
📂 GitHub Repository: Public

---

📌 Problem Statement

In India, 90% of people sign legal documents (Rent Agreement, Job Contracts, NDA) without understanding the terms because they are written in complex English legal jargon. This leads to exploitation, especially in Tamil Nadu where English is not primary. There is no affordable tool that generates legally sound documents AND explains them in local Tanglish.

💡 Our Solution - LegalEase

LegalEase is a full-stack AI platform that:
1.  **GENERATES** professional legal documents from simple user inputs.
2.  **EXPLAINS** each clause in simple English + Tanglish (Tamil + English mix).
3.  **EXPORTS** final document into PDF & DOCX format with proper formatting.

We are making Law Accessible for Everyone.

✨ Key Features

1. Intelligent Document Generation
- **Lease / Rental Agreement:** Landlord, Tenant, Rent, Deposit, Duration
- **Non-Disclosure Agreement (NDA):** Company, Receiving Party, Confidential Info
- **Employment Contract:** Company, Employee, Salary, Role, Joining Date
- Dynamic template filling using LLM + `python-docx`

2. Bilingual Legal Simplifier (Our USP)
For every generated document, we provide a side-by-side explanation:
- **English Explanation:** Simple 8th-grade English
- **Tanglish Explanation:** "Idha paatha, ithu solrathu enna na, veetu owner-ku damage panna neenga thaan poruppu-nu artham"

3. Professional Export
- `FPDF` for clean PDF generation with header/footer
- `python-docx` for editable Word file
- Supports A4 formatting, font styling, signature blocks

4. AI Validation
- Checks for missing fields
- Suggests better legal phrasing using Gemini 1.5 Pro
- Detects risky clauses

🏗️ System Architecture

User Input (Streamlit Form) -> FastAPI Backend -> Gemini 1.5 Pro API
                                       |
                                       v
                         Prompt Engineering + Template Engine
                                       |
                                       v
                    [DOCX Generation] + [PDF Conversion] + [Tanglish Explanation]
                                       |
                                       v
                          Streamlit UI (Preview + Download)

🛠️ Tech Stack - In Detail

| Layer | Technology | Reason for Choosing |
| :--- | :--- | :--- |
| **LLM / AI** | Google Gemini 1.5 Pro | Best for long-context legal reasoning, free tier, supports Tamil |
| **Backend** | FastAPI (Python) | Fast, async, auto API docs |
| **Frontend** | Streamlit | Rapid prototyping, Python native |
| **Doc Gen** | python-docx, FPDF2 | Industry standard for doc creation |
| **Prompt Eng**| Few-shot + Role-based prompting | To get consistent legal format |
| **Env Mgmt** | python-dotenv | For API key security |

⚙️ How to Run Locally (Setup Guide)

**Prerequisites:** Python 3.10+, Gemini API Key

1.  **Clone the Repository**
    ```bash
    git clone https://github.com/janarthanaa/LegalEase.git
    cd LegalEase
2.  *Create Virtual Environment*
    python -m venv venv
    source venv/bin/activate # or venv\Scripts\activate on Windows
3.  *Install Dependencies*
    pip install -r requirements.txt
4.  *Add API Key*
    Create a `.env` file in root:
    GEMINI_API_KEY=YOUR_API_KEY_HERE
5.  *Run Backend*
    uvicorn main:app --reload --port 8000
6.  *Run Frontend*
    streamlit run app.py
📂 Project Structure
LegalEase/
├── main.py              # FastAPI backend - /generate endpoint
├── app.py               # Streamlit frontend
├── templates/
│   ├── lease_template.docx
│   ├── nda_template.docx
│   └── employment_template.docx
├── utils/
│   ├── doc_generator.py # docx & pdf logic
│   └── explainer.py     # Gemini Tanglish logic
├── requirements.txt
├── .env.example
└── README.md
🚀 Future Scope

1.  Voice-based Tanglish Explanation (Text-to-Speech)
2.  Add more languages: Hindi, Malayalam
3.  Blockchain-based e-Signature Integration
4.  Lawyer Verification Marketplace

👥 Team Details

- *Team Leader:* JANARTHANAA - Architecture, Backend & AI Integration
- *Team Member 1:* RAMANATHAN - Frontend Development (Streamlit) & UI/UX
- *Team Member 2:* PANDIDURAI - Documentation, Testing & Template Design

*College:* [Jesu college of arts and science,alangudi.]
*Department:* [BSC.COMPUTER SCIENCE]

🏆 Built For

*AICTE - Skill Wallet Project Submission 2026*
*Theme: AI for Social Good & Accessibility*

---
> _We didn't just build a document generator, we built legal awareness._
