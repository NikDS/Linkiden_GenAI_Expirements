# 🤖 LinkedIn GenAI Experiments

A practical exploration into using Generative AI and automation to understand the latest skill trends across job titles on LinkedIn. This project combines **web scraping**, **natural language processing**, and **large language models** to extract and analyze job requirements at scale.

---

## 🎯 Objective

> Learn how to use, play with, and code GenAI tools to explore job trends.

The goal is to:
- Scrape job descriptions from LinkedIn for any given job title.
- Analyze and summarize trending skill sets using LLMs.
- Help professionals stay up to date in their field by extracting actionable insights.

---

## 🛠️ Technologies Used

- **Python**
- **Selenium** – for LinkedIn job scraping
- **LangChain** – for prompt templating and chunking
- **Ollama** – to run LLMs like LLaMA locally
- **pandas**, **logging** – for data manipulation and logging

---

## 🚀 How It Works

### 🔍 Part 1 – Job Scraping (Selenium)

- Logs into LinkedIn (requires `credentials.txt` with username/password)
- Searches jobs based on user input (e.g., `"Data Scientist"`)
- Extracts job title, company, location, and description
- Saves results into `linkedin_jobs_detailed v1.csv`

### 🧠 Part 2 – Trend Extraction (GenAI + LangChain)

- Loads job descriptions from CSV
- Chunks them using LangChain's `RecursiveCharacterTextSplitter`
- Uses a local LLM (via Ollama) to:
  - Extract technical skillsets
  - Rank and summarize most important ones
- Outputs the top 10 most in-demand skills with commentary



## 🔑 Setup Instructions

### 1. Install Python Packages

```bash
pip install selenium pandas langchain langchain-community ollama
```

Also install [Ollama](https://ollama.com/) and run:

```bash
ollama run llama3
```

### 2. Create Your `credentials.txt` File

```
your_email@example.com
your_linkedin_password
```

### 3. Run the Scripts

#### Step 1: Scrape LinkedIn Jobs

> You'll be prompted for the job title you want to search.

#### Step 2: Analyze Skill Trends

## 📌 Notes

- You must have Chrome and ChromeDriver installed.
- Make sure your LinkedIn account has access to the job section.
- Ollama must be running before invoking the LLM scripts.

---

## 🙏 Acknowledgements

- LinkedIn for providing access to job listings
- LangChain & Ollama teams for enabling powerful local GenAI workflows

---

## 📄 License

MIT License

```
MIT License

Copyright (c) 2025 Nikhil Rajyaguru

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in the
Software without restriction, including without limitation the rights to use, copy,
modify, merge, publish, distribute, sublicense, and/or sell copies of the Software,
and to permit persons to whom the Software is furnished to do so, subject to the
following conditions:

The above copyright notice and this permission notice shall be included in all copies
or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED,
INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR
PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE
FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR
OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
DEALINGS IN THE SOFTWARE.
```
