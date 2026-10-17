# llm-zoomcamp-2026-code

My code for the [LLM Zoomcamp](https://github.com/DataTalksClub/llm-zoomcamp) course.

## Structure

```
├── 01-agentic-rag/            # Module 1 notebooks (course work)
├── homework/                  # Homework solutions, one folder per module
│   └── 01-agentic-rag/
├── src/llm_zoomcamp_2026_code/  # Reusable code shared across modules
│   ├── ingest.py              # load_faq_data, build_index
│   └── rag_helper.py          # RAGBase
├── pyproject.toml
└── uv.lock
```

New modules get their own top-level folder (`02-vector-search/`, `03-orchestration/`, ...),
with a matching folder under `homework/`.

## Setup

```bash
uv sync
```

Put your API keys in a `.env` file at the repo root. Shared helpers are installed as a package, so any notebook can import them:

```python
from llm_zoomcamp_2026_code.ingest import load_faq_data, build_index
from llm_zoomcamp_2026_code.rag_helper import RAGBase
```
