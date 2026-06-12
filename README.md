# AI Resume Analyzer 🤖

A modern, high-performance Streamlit application that extracts text from uploaded PDF resumes and performs hybrid skill matching (exact keyword matching + semantic AI similarity search) against a customizable list of job description skills. The app visualizes candidate matches, generates comparative charts, and provides downloadable analysis reports.

## 🚀 Features

- **Multi-Resume Upload**: Drag and drop multiple PDF resumes to analyze them concurrently.
- **Hybrid Skill Matching**:
  - **Keyword Match**: Precise exact-match checking.
  - **Semantic AI Match**: Sentence-transformer-based embedding search (`all-MiniLM-L6-v2`) to capture contextually relevant experience, even if they use different phrasing.
- **Interactive Visualizations**:
  - Overview cards showing candidate match rates.
  - Candidate comparison bar charts.
  - Skills comparison tables.
  - Interactive radar charts comparing candidate competencies.
  - Donut charts for individual resume match breakdowns.
- **Downloadable Reports**: Generate and download structured TXT analysis reports for each candidate.

---

## 💻 Local Setup & Development

1. **Clone the repository**:
   ```bash
   git clone https://github.com/prashantgangwar18/ai-resume-analyser.git
   cd ai-resume-analyser
   ```

2. **Create a virtual environment (optional but recommended)**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Streamlit app**:
   ```bash
   streamlit run shortlister3.py
   ```

---

## 🌐 Deployment to Render

This repository is optimized for deployment to **Render** using a CPU-only environment to keep builds fast and resource usage within limits.

### Configuration on Render:

1. Create a new **Web Service** on Render.
2. Link your GitHub repository `ai-resume-analyser`.
3. Configure the following service settings:
   - **Environment**: `Python`
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `streamlit run shortlister3.py --server.port $PORT --server.address 0.0.0.0`
4. Choose the free/starter tier and deploy.