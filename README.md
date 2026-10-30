# Financial Document Intelligence Platform

Ask questions about financial documents and get answers with cited sources. A fine-tuned sentiment model classifies passages, and a LangGraph agent combines it with document search.

> **Status:** in development. **Informational only.** This project does not give investment advice or buy/sell signals.

## What it does

- **Classify:** a DistilBERT model fine-tuned in PyTorch labels passages as positive, neutral or negative.
- **Answer:** a LangChain RAG pipeline answers questions about uploaded documents. Every answer shows its source passage and page.
- **Agent:** a LangGraph agent can search documents, run the sentiment model and compare companies.
- **Dashboard:** sentiment and risk signals over time, per company.

## Architecture

_Diagram goes here once the pieces exist._

| Part | Tool |
|---|---|
| Classifier | PyTorch, Hugging Face Transformers |
| Retrieval | LangChain, Chroma |
| Agent | LangGraph |
| API | FastAPI |
| Dashboard | React |
| Packaging | Docker |

## Data

- **Training:** Financial PhraseBank (licence: to be checked before use).
- **Documents:** public filings, such as SEC EDGAR annual reports and earnings material.
- Public data only. No personal or bank data.

## Results

| Metric | Result |
|---|---|
| Classifier F1 vs TF-IDF + logistic regression baseline | not measured yet |
| RAG answer accuracy (about 50 hand-written questions) | not measured yet |
| Latency and cost per query | not measured yet |

## Tradeoffs

_Filled in as decisions are made: LLM choice (hosted vs local), deployment, model size._

## Setup

Requires Python 3.12.

```bash
py -3.12 -m venv .venv
.venv\Scripts\activate
```

## Demo

_Live demo link and GIF go here._