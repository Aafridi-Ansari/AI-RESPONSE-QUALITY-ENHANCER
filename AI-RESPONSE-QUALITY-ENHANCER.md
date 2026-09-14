# AI Response Quality Evaluator Agent & Evaluation Platform

An end-to-end multi-agent evaluation platform for assessing AI response quality across Relevance, Accuracy & Grounding, Completeness, and Hallucination metrics. Includes a FastAPI backend with RAG vector search capabilities, automated PDF report generation, and a modern React/Vite analytics dashboard.

---

## 📁 Repository Architecture

```
eval_platform/
├── docs/                        # Documentation and guides
│   ├── Agile.xls                # Agile project backlog
│   ├── Defect_Tracker.xlsx      # Defect tracking log
│   ├── Unit_Test_Plan.xlsx      # Unit test suite documentation
│   ├── Balakumaran_S_S_project_report.pdf
│   ├── Balakumaran_S_S_technical_documentation.pdf
│   └── two_system_comparison.csv
├── eval_platform_backend/       # Backend API, Agents, and RAG logic
│   ├── main.py                  # Entry point (FastAPI / Uvicorn server)
│   ├── requirements.txt         # Backend dependencies
│   ├── src/
│   │   ├── agents/              # Multi-agent evaluator definitions
│   │   ├── api/                 # FastAPI routes & OAuth2 JWT auth
│   │   ├── database/            # SQLAlchemy database models & config
│   │   ├── rag/                 # ChromaDB vector store retriever
│   │   └── reporting/           # ReportLab PDF report generation
│   ├── test_batch_api.py
│   ├── test_eval_agents.py
│   ├── verify_agents.py
│   └── verify_pipeline.py
└── eval_platform_frontend/      # Frontend Dashboard (React/Vite)
    ├── package.json             # Frontend dependencies
    ├── index.html
    ├── vite.config.js
    ├── eslint.config.js
    ├── public/                  # Static assets & icons
    └── src/
        ├── components/          # Dashboard UI components
        ├── pages/               # Dashboard pages
        ├── App.css
        ├── App.jsx
        ├── index.css            # Global styling
        └── main.jsx
```

---

##  Quick Start Guide

### 1. Backend Setup (FastAPI)

```bash
cd eval_platform_backend

# Install dependencies
pip install -r requirements.txt

# Start FastAPI server
python main.py
```
The API server will run at `http://localhost:8000`. Interactive API docs are available at `http://localhost:8000/docs`.

### 2. Frontend Setup (React / Vite)

```bash
cd eval_platform_frontend

# Install dependencies
npm install

# Run Vite dev server
npm run dev
```
Access the dashboard in your browser at `http://localhost:5173`.

---

## 📄 Documentation & Artifacts

All project artifacts are located in the `docs/` folder:
- **`Balakumaran_S_S_project_report.pdf`**: Complete Project Report
- **`Balakumaran_S_S_technical_documentation.pdf`**: System Architecture & Technical Documentation
- **`Agile.xls`**: Product and Sprint Backlogs
- **`Defect_Tracker.xlsx`**: Logged defects and resolutions
- **`Unit_Test_Plan.xlsx`**: Test cases and execution metrics
- **`two_system_comparison.csv`**: Sample dataset comparing LLM evaluation outputs
