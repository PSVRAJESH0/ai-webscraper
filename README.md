
# 🕸️ AI Web Scraper with Streamlit + LLM

This project is a simple web scraping tool with an AI-powered interface that:
- Scrapes websites using Selenium (locally).
- Extracts and cleans DOM `<body>` content.
- Uses a Large Language Model (via LangChain + Ollama) to parse and extract meaningful data based on user-defined queries.
- Provides an interactive frontend with **Streamlit**.

---

## 🚀 Features

- 🔗 Scrape any public webpage by entering its URL
- 🧠 Ask questions like:  
  *"Extract all product names and prices"* or  
  *"Get all headings and descriptions"*
- ⚙️ Works with **local Chrome browser** using Selenium
- 📄 Clean and chunk DOM content for efficient processing
- 🗨️ Uses **LLaMA 3** locally with **Ollama** and **LangChain**

---

## 📦 Requirements

Install dependencies:

```bash
pip install -r requirements.txt
```

> 💡 If using `webdriver-manager`, install it manually:
```bash
pip install webdriver-manager
```

Make sure you have:
- [Google Chrome](https://www.google.com/chrome/) installed.
- [ChromeDriver](https://sites.google.com/chromium.org/driver/) matching your Chrome version, or use `webdriver-manager`.
- [Ollama](https://ollama.com/) installed and running a local model (e.g., `llama3`).

---

## 🛠 Project Structure

```
├── main.py             # Streamlit frontend
├── scrape.py           # Web scraping and cleaning
├── parse.py            # LLM prompt and parsing logic
├── requirements.txt    # Python dependencies
└── README.md           # Project documentation
```

---

## 🖥️ Usage

1. Start your Ollama model (e.g., llama3):
```bash
ollama run llama3
```

2. Run the Streamlit app:
```bash
streamlit run main.py
```

3. In the browser:
   - Enter a website URL.
   - Click **"Scrape Website"**.
   - Describe what to parse (e.g., "Extract all links and their text").
   - Click **"Parse Content"**.

---

## 📚 Example Queries

- `List all the headings on the page.`
- `Extract all links with their anchor text.`
- `Get product names and prices.`

---

## 🔒 Limitations

- CAPTCHA-protected sites may block scraping.
- Pages with heavy JavaScript rendering may load incomplete content.
- Ollama model memory requirements can be high (6+ GB RAM).

---

## 📜 License

This project is licensed under the MIT License.

---

## 🤝 Credits

- Built with [Streamlit](https://streamlit.io/)
- LLM integration via [LangChain](https://www.langchain.com/)
- Model served with [Ollama](https://ollama.com/)
- Scraping done using [Selenium](https://www.selenium.dev/) + [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/)
