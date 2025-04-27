# sheet-sql-chatbot

📄💬 Google Sheet Q&A SQL Bot
Ask natural-language questions of any public Google Sheet—and see both the auto-generated SQL and the query results—powered by a free OpenRouter model and DuckDB.

🔍 What it does
Load a public Google Sheet (via CSV export).

Inspect the column names and sample data.

Enter an English question (e.g., “What was the average sales in Q1 2024?”).

Translate your question to a DuckDB SELECT statement using a free OpenRouter LLM.

Execute the SQL in-memory via DuckDB and display the result.

Download the result as a CSV.

Demo only—public sheets, single worksheet, no authentication.
For enterprise BI chat with SSO, multi-table joins, or caching, contact me.

✨ Key Features
Zero credentials: works with any Google Sheet published to web.

Transparent SQL: shows you the exact SELECT statement generated.

In-memory DuckDB: lightning-fast analytics without external databases.

Full conversational history: context-aware follow-up questions.

Downloadable: export your query results to CSV.

🔑 Add your OpenRouter API key
Streamlit Cloud
Go to the app’s ⋯ → Edit secrets.

Add:

toml
Copy
Edit
OPENROUTER_API_KEY = "sk-or-xxxxxxxxxxxxxxxx"
Local development
Create ~/.streamlit/secrets.toml:

toml
Copy
Edit
OPENROUTER_API_KEY = "sk-or-xxxxxxxxxxxxxxxx"
—or—

bash
Copy
Edit
export OPENROUTER_API_KEY=sk-or-xxxxxxxxxxxxxxxx
🚀 Quick Start (Local)
bash
Copy
Edit
git clone https://github.com/THartyMBA/sheet-sql-chatbot.git
cd sheet-sql-chatbot
python -m venv venv && source venv/bin/activate   # On Windows: venv\Scripts\activate
pip install -r requirements.txt
streamlit run sheet_sql_chatbot.py
Open http://localhost:8501.

Paste your public Sheet URL or ID.

Ask your question and explore the SQL + results.

☁️ Deploy on Streamlit Community Cloud
Push this repo (public or private) under THartyMBA to GitHub.

Go to streamlit.io/cloud → New app → select your repo & branch.

Add OPENROUTER_API_KEY in Secrets.

Click Deploy—no further config.

🛠️ Requirements
shell
Copy
Edit
streamlit>=1.32
pandas
duckdb
requests
(No heavy ML libraries; runs on the free tier CPU.)

🗂️ Repo Structure
kotlin
Copy
Edit
sheet-sql-chatbot/
├─ sheet_sql_chatbot.py   ← single-file Streamlit app
├─ requirements.txt
└─ README.md              ← this file
📜 License
CC0 1.0 – public-domain dedication. Attribution appreciated but not required.

🙏 Acknowledgements
Streamlit – rapid Python apps

OpenRouter – free LLM gateway

DuckDB – in-memory analytics

Google Sheets public CSV export – no-key data access

Query your sheets with SQL—chat style! 🚀
