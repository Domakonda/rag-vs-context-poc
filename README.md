# RAG vs Full-Context POC

Local Streamlit chat app that answers the same question two ways and compares them:

- **RAG**: retrieve the top-k chunks from ChromaDB and send only those to the LLM.
- **Full context**: send the whole CSV/JSON dataset to the LLM.
- **Compare**: run both side by side with timing, token and cost metrics.

Stack: Python 3.12, uv, Streamlit, OpenAI API (LLM + `text-embedding-3-small`), ChromaDB.

## Setup

```
uv sync
cp .env.example .env   # then add your OPENAI_API_KEY
```

Settings live in `ragchat.config.json`.

## Run (once implemented)

```
uv run ragchat ingest --reset
uv run streamlit run app.py
```

Status: project scaffold only; app code not written yet.
