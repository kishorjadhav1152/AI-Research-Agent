# 🤖 AI Research Agent — LangGraph

An **Agentic AI Research Assistant** built using **LangGraph, LangChain, Google Gemini, arXiv, Streamlit, and Python**.

This project helps users research a topic by searching academic papers, reading research PDFs, analyzing research content, identifying potential research directions, and generating research-paper drafts in LaTeX/PDF format.

---

## 🚀 Features

* 🔎 **Research Paper Search** — Search academic papers from arXiv.
* 📚 **PDF Research Analysis** — Extract and analyze content from research papers.
* 🧠 **Agentic AI Workflow** — Uses LangGraph to manage the research workflow.
* 🤖 **Google Gemini Integration** — Uses Gemini for research analysis and generation.
* 💡 **Research Direction Generation** — Generates potential research ideas based on existing papers.
* ✍️ **Research Paper Generation** — Generates structured research-paper content using LaTeX.
* 📄 **PDF Generation** — Converts LaTeX research papers into PDF documents.
* 💬 **Streamlit Interface** — Interactive web interface for communicating with the research agent.

---

## 🏗️ Project Architecture

```text
                         ┌─────────────────┐
                         │      User       │
                         └────────┬────────┘
                                  │
                                  ▼
                         ┌─────────────────┐
                         │  Streamlit UI   │
                         └────────┬────────┘
                                  │
                                  ▼
                         ┌─────────────────┐
                         │   LangGraph     │
                         │  Research Agent │
                         └────────┬────────┘
                                  │
              ┌───────────────────┼───────────────────┐
              │                   │                   │
              ▼                   ▼                   ▼
       ┌─────────────┐     ┌─────────────┐     ┌─────────────┐
       │ arXiv Search│     │  PDF Reader │     │ PDF Writer  │
       │    Tool     │     │    Tool     │     │   /LaTeX    │
       └──────┬──────┘     └──────┬──────┘     └──────┬──────┘
              │                   │                   │
              └───────────────────┼───────────────────┘
                                  │
                                  ▼
                         ┌─────────────────┐
                         │  Google Gemini  │
                         │       LLM       │
                         └─────────────────┘
```

---

## 🛠️ Technologies Used

| Technology    | Purpose                      |
| ------------- | ---------------------------- |
| Python        | Core programming language    |
| LangGraph     | Agent workflow orchestration |
| LangChain     | LLM and tool integration     |
| Google Gemini | Large Language Model         |
| arXiv         | Research paper search        |
| Streamlit     | Web interface                |
| PyPDF2        | PDF text extraction          |
| Tectonic      | LaTeX to PDF conversion      |
| uv            | Python dependency management |

---

## 📂 Project Structure

```text
AI-Research-Agent/
│
├── ai_researcher_2.py      # Main LangGraph research agent
├── arxiv_tool.py           # arXiv research paper search
├── frontend.py             # Streamlit application
├── read_pdf.py             # PDF reading and text extraction
├── write_pdf.py            # LaTeX/PDF generation
│
├── pyproject.toml           # Project dependencies and configuration
├── uv.lock                  # Locked dependency versions
│
├── .env.example             # Environment variable template
├── .gitignore               # Git ignored files
└── README.md                # Project documentation
```

---

# ⚙️ Installation

## 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/AI-Research-Agent.git
```

Move into the project directory:

```bash
cd AI-Research-Agent
```

---

## 2. Create Environment Variables

Create a `.env` file in the project root.

```env
GOOGLE_API_KEY=your_google_gemini_api_key
```

You can use `.env.example` as a template.

### ⚠️ Security

**Never upload your `.env` file or API key to GitHub.**

The `.gitignore` file is configured to prevent `.env` from being committed.

---

## 3. Install Dependencies

If you are using **uv**:

```bash
uv sync
```

Alternatively, install the project using pip:

```bash
pip install -e .
```

---

## 4. Install Tectonic

This project uses **Tectonic** to compile LaTeX documents into PDF files.

Verify that Tectonic is installed:

```bash
tectonic --version
```

Make sure the `tectonic` command is available in your system PATH.

---

# ▶️ Running the Application

Start the Streamlit application:

```bash
uv run streamlit run frontend.py
```

Or:

```bash
streamlit run frontend.py
```

The application will open in your browser.

Usually, Streamlit runs at:

```text
http://localhost:8501
```

---

# 🔬 How the AI Research Agent Works

### Step 1 — Enter Research Topic

The user enters a research topic or question.

Example:

```text
Large Language Models for Financial Risk Prediction
```

### Step 2 — Search Research Papers

The agent searches arXiv for relevant academic papers.

### Step 3 — Read Research Papers

The PDF reader extracts the content of selected research papers.

### Step 4 — Analyze Research

Google Gemini analyzes the research content and helps identify:

* Research methodology
* Key findings
* Limitations
* Important concepts
* Potential research gaps

### Step 5 — Generate Research Directions

The agent generates possible research directions based on the analyzed literature.

### Step 6 — Generate Research Paper

The system can generate structured research-paper content using LaTeX.

### Step 7 — Generate PDF

The LaTeX document can be compiled into a PDF using Tectonic.

---

# 💡 Example Use Case

```text
User:
"Research recent approaches for AI-based credit risk prediction."

              ↓

        LangGraph Agent

              ↓

        Search arXiv Papers

              ↓

       Read Selected Papers

              ↓

       Analyze Literature

              ↓

      Identify Research Gaps

              ↓

     Generate Research Ideas

              ↓

      Generate LaTeX Paper

              ↓

          PDF Output
```

---

# 🔑 Environment Variables

Create a `.env` file:

```env
GOOGLE_API_KEY=your_google_gemini_api_key
```

Do not commit this file.

Use `.env.example` when sharing the project.

---

# 📌 Important Notes

* An internet connection is required for accessing arXiv and Google Gemini.
* A valid Google Gemini API key is required.
* Tectonic must be installed separately.
* Generated research content should be reviewed by a human.
* Always verify research claims, references, equations, and citations before academic or professional use.
* Respect the licensing and usage requirements of papers retrieved from external sources.

---

# 🔐 Security

Never upload sensitive information such as:

```text
.env
API keys
Passwords
Access tokens
Private research documents
Credentials
```

If an API key is accidentally committed to GitHub, revoke/rotate the key immediately.

---

# 🚧 Future Improvements

Possible future enhancements include:

* [ ] Add persistent research history
* [ ] Add research-paper citation management
* [ ] Add paper comparison functionality
* [ ] Add automatic bibliography generation
* [ ] Add automated testing
* [ ] Add Docker support
* [ ] Add cloud deployment
* [ ] Add downloadable research reports
* [ ] Add support for additional academic databases
* [ ] Improve multi-agent research workflow

---

# 📜 License

This project can be released under the **MIT License**.

If you choose MIT, add an `LICENSE` file to the repository before publishing.

---

# 👨‍💻 Author

**Kishor Jadhav**

AI / Machine Learning | Data Science | Agentic AI

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.
