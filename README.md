Below is a **production-ready `README.md`** you can directly push to GitHub.
I’ve written it as a senior developer would: clear overview, setup steps, environment configuration, and explicit instructions for **Ollama** and **Gemini API key**.

---

# Company Brochure Generator (AI-Powered)

An **AI-powered company sales brochure generator** that scrapes website content and generates professional marketing brochures using **LLMs** such as **Google Gemini** and **Ollama (local models)**.

This project is designed to:

* Scrape and clean website content
* Extract meaningful company information
* Generate AI-driven sales brochures
* Support both **cloud-based** (Gemini) and **local** (Ollama) LLM workflows

---

## Features

* 🌐 Website content scraping using `BeautifulSoup`
* 🤖 AI brochure generation
* 🔑 Supports **Google Gemini API**
* 🖥️ Supports **Ollama local models**
* 📦 Clean Python project structure with `pyproject.toml`

---

## Tech Stack

* **Python 3.11**
* BeautifulSoup4
* Requests
* Google Generative AI (Gemini)
* Ollama
* Pandas / NumPy

---

## Project Structure

```text
.
├── scraper.py                  # Website scraping logic
├── Broucher_Generater_Gemini.ipynb
├── Broucher_Generater_ollama.ipynb
├── requirements.txt
├── pyproject.toml
└── README.md
```

---

## Prerequisites

* Python **3.11.x**
* Git
* Internet connection (for Gemini)
* At least **8 GB RAM** recommended for Ollama models

---

## Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/upratham/Company-Broucher-Generator.git
cd Company-Broucher-Generator
```

---

### 2️⃣ Create a Virtual Environment (Recommended)

```bash
python -m venv venv
```

Activate it:

* **Windows**

```bash
venv\Scripts\activate
```

* **macOS / Linux**

```bash
source venv/bin/activate
```

---

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

or using `pyproject.toml`:

```bash
pip install .
```

---

## Environment Variables Setup

Create a `.env` file in the project root:

```env
GEMINI_API_KEY=your_gemini_api_key_here
```

---

## 🔑 How to Obtain a Google Gemini API Key

1. Go to **Google AI Studio**
   👉 [https://aistudio.google.com/](https://aistudio.google.com/)

2. Sign in with your Google account

3. Click **“Get API Key”**

4. Create a new API key

5. Copy the key and add it to your `.env` file:

```env
GEMINI_API_KEY=AIzaSyXXXXXXXXXXXX
```

---

## 🦙 Installing and Using Ollama (Local LLM)

### Step 1: Install Ollama

Download Ollama from the official site:

👉 [https://ollama.com/download](https://ollama.com/download)

Supported platforms:

* Windows
* macOS
* Linux

---

### Step 2: Verify Installation

```bash
ollama --version
```

---

### Step 3: Pull a Model

Example: Pull **Llama 3**

```bash
ollama pull llama3
```

Other popular models:

```bash
ollama pull mistral
ollama pull gemma
```

---

### Step 4: Run Ollama Server

Ollama runs automatically in the background once installed.

To verify:

```bash
ollama list
```

---

## Running the Project

### ▶ Using Gemini (Cloud LLM)

Open and run:

```bash
jupyter notebook Broucher_Generater_Gemini.ipynb
```

Make sure:

* Internet connection is active
* `GEMINI_API_KEY` is correctly set

---

### ▶ Using Ollama (Local LLM)

Open and run:

```bash
jupyter notebook Broucher_Generater_ollama.ipynb
```

Ensure:

* Ollama is running
* Required model is already pulled

---

## Scraper Usage

`scraper.py` provides utility functions to:

* Fetch website content (title + cleaned text)
* Extract hyperlinks

Example usage:

```python
from scraper import fetch_website_contents

content = fetch_website_contents("https://example.com")
print(content)
```

---

## Common Issues & Fixes

### ❌ Gemini API Error

* Ensure API key is valid
* Check `.env` file is loaded
* Restart notebook after setting env vars

### ❌ Ollama Model Not Found

```bash
ollama pull <model-name>
```

### ❌ SSL / Requests Errors

```bash
pip install --upgrade requests certifi
```

---

## Future Enhancements

* PDF brochure export
* Multi-language brochure generation
* SEO-optimized content
* Batch website processing
* Fine-tuned local models

---

## Author

**Prathamesh Uravane**
📧 [upratham2002@gmail.com](mailto:upratham2002@gmail.com)

---

## License

This project is licensed under the **MIT License**.

