 # PubMed Paper Fetcher CLI Tool

## 📄 Overview

This project is a Python-based command-line tool that fetches research papers from PubMed based on a user-defined query and filters the authors affiliated with non-academic institutions such as pharmaceutical or biotech companies.

It was developed as part of a take-home backend assessment to demonstrate API integration, XML parsing, command-line interface (CLI) design, and modular Python development using Poetry.

---

## ✅ Features

* 🔍 Query PubMed using full search syntax
* 📄 Retrieve and parse metadata using `esearch` and `efetch` endpoints
* 🧠 Filter authors by non-academic affiliations using keyword-based heuristics
* 📤 Export filtered paper metadata to CSV format
* ⚙️ Fully modular and maintainable codebase
* 🐍 Built with Python 3.11 and managed with Poetry
* 🧪 Includes debug logging and error handling

---

## 🛠 Tech Stack & Tools

* **Python 3.11**
* **Poetry** – Dependency management
* **requests** – For PubMed API communication
* **argparse** – CLI parsing
* **xml.etree.ElementTree** – XML parsing
* **csv** – CSV file creation
* **Git + GitHub** – Version control

---

## 📂 Project Structure

```
get_papers/
├── get_papers/
│   ├── __init__.py
│   ├── api.py           # Handles PubMed API calls
│   ├── parser.py        # XML parsing logic
│   ├── filter.py        # Affiliation filtering
│   ├── exporter.py      # CSV export logic
│   └── cli.py           # Command-line interface
├── main.py              # Entrypoint
├── pyproject.toml       # Poetry config
├── README.md
└── tests/               # Optional test cases
```

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/pubmed-paper-fetcher.git
cd pubmed-paper-fetcher
```

### 2. Install Dependencies

```bash
poetry install
```

### 3. Run the Tool

```bash
poetry run python main.py --query "cancer immunotherapy" --file results.csv
```

#### Optional Flags

* `--debug` – Enable debug logging
* `--help` – Show CLI usage help

---

## 📊 CSV Output Format

The exported CSV file includes:

* Title
* Journal
* Publication Date
* Authors
* Affiliations
* PubMed ID
* Link

---

## 🧠 Filtering Logic

Authors are classified as "non-academic" based on their affiliation strings containing keywords like:

* "Inc", "Ltd", "LLC", "Pharma", "Biotech", etc.

And **excluding** academic terms like:

* "University", "College", "Institute", etc.

---

## 📌 Notes

* PubMed has usage limits. Use debug mode to troubleshoot if API limits are hit.
* This is an academic prototype. For large-scale use, implement error retries and PubMed’s API key system.

---

## 👤 Author

**Gayatri Dhumal**
Python Developer | Backend Enthusiast
\[Your GitHub Profile URL]

---

## 🔗 Links

* **GitHub Repo**: \[Insert GitHub URL here]
* **ChatGPT Session**: \[Insert Link Here]

---

## 🏁 License

This project is provided for educational/demo purposes and is not intended for production without modification.
