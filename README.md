
# 🧠 MindPulse AI — Clinical Affective Telemetry Platform

MindPulse AI is an edge-focused, privacy-first mental health screening and journal analytics platform built for real-time risk mitigation, transparent sentiment evaluation, and multi-modal clinical telemetry.

---

## 🚀 Key Features & Innovations

1. 📝 **Real-Time XAI Span Tagging**
   * Parses journal input using explainable NLP rules to highlight cognitive and emotional markers:
     * 🔴 **Absolute Language:** Highlights rigid cognitive patterns (always, never, no one, every time).
     * 🟡 **Somatic & Fatigue Signals:** Color-codes physical strain indicators (exhausted, tired, drained, insomnia).
     * 🟣 **Cognitive Distortion:** Pinpoints negative affective biases (worthless, failure, disaster, ruined).

2. 📋 **Standardized Clinical Psychometrics**
   * **Automated Screening:** Built-in interactive calculators for standard 9-item PHQ-9 (Depression) and 7-item GAD-7 (Anxiety) inventories.
   * **Clinical Export:** 1-Click HIPAA-compliant client reporting export.

3. 👁️ **Edge Multimodal Telemetry**
   * **Visual:** Real-time 3D facial mesh & FACS Action Unit tracking via MediaPipe.
   * **Audio:** Client-side 40-band Mel-Spectrogram acoustic analysis.

---

## 🛠️ Technology Stack

| Domain | Framework / Library | Purpose |
| :--- | :--- | :--- |
| **Backend API** | FastAPI (Python 3.10+) | High-performance asynchronous REST API orchestration |
| **Server / WSGI** | Uvicorn | Production-grade ASGI server implementation |
| **NLP & XAI Engine** | Scikit-Learn / Regex | Rule-based explainable span tagging & affective classification |
| **Audio Processing** | Web Audio API (AnalyserNode) | Real-time client-side 40-band Mel-Spectrogram generation |
| **Visual Telemetry** | MediaPipe / WebGL | 3D Facial Mesh and FACS Action Unit tracking |
| **Frontend UI** | HTML5, Modern CSS3, Vanilla JS | Lightweight, zero-dependency responsive client interface |
| **PDF Reporting** | jsPDF | HIPAA-compliant client-side clinical report export |
| **Cloud Hosting** | Render | Automatic continuous deployment web service hosting |

---

## 💻 Local Development Setup

### Prerequisites
* **Python**: 3.10 or higher
* **Git**: Installed on your system
* **Node.js / npm**: (Optional) Required only if managing root dependency packages

### Step-by-Step Installation

1. **Clone the Repository**
   git clone [https://github.com/harshitr31/MindPulse_AI.git](https://github.com/harshitr31/MindPulse_AI.git)
   cd MindPulse_AI

2. **Create & Activate Virtual Environment**
   * **Windows (PowerShell):**
     python -m venv venv
     .\venv\Scripts\Activate.ps1
   * **Linux / macOS:**
     python3 -m venv venv
     source venv/bin/activate

3. **Install Backend Dependencies**
   pip install fastapi uvicorn scikit-learn numpy librosa soundfile torch jspdf

4. **Launch the Development Server**
   python -m uvicorn backend.main:app --host 127.0.0.1 --port 8000 --reload

5. **Access Local Endpoints**
   * **Dashboard & Studio:** Open [http://127.0.0.1:8000/](http://127.0.0.1:8000/) in your browser.
   * **Interactive REST Docs:** Navigate to [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs) to inspect and test API routes.'

## 📂 Repository Structure

```text
MindPulse_AI/
├── 📁 backend/                      # FastAPI Backend Service
│   ├── 📁 app/
│   │   ├── 📁 api/                  # API endpoints and route handlers
│   │   ├── 📁 core/                 # Configs, security, and environment settings
│   │   ├── 📁 models/               # ML model loaders and inference pipelines
│   │   └── 📁 services/             # Psycholinguistic and biomarker extractors
│   ├── main.py                      # Application entry point & CORS configuration
│   └── requirements.txt             # Python dependencies (FastAPI, Torch, Scikit-Learn)
│
├── 📁 frontend/                     # React + Vite Frontend UI
│   ├── 📁 public/                   # Static assets, icons, and favicon
│   ├── 📁 src/
│   │   ├── 📁 components/           # UI components (Charts, Gauge, Forms)
│   │   ├── 📁 pages/                # App views (Journal, Telemetry, Screener, Grounding)
│   │   ├── 📁 styles/               # Global CSS & Tailwind configurations
│   │   ├── App.jsx                  # Main routing & state layout
│   │   └── main.jsx                 # React DOM mount point
│   ├── index.html                   # HTML template entry
│   ├── package.json                 # Node.js dependencies & build scripts
│   └── vite.config.js               # Vite bundler & dev server config
│
├── .gitignore                       # Rules excluding venv/, node_modules/, and cache
└── README.md                        # Project documentation and architecture guide