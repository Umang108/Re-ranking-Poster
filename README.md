# 🔁 What is Reranking? — Visual Poster

A dark-themed, chalkboard-style educational poster explaining **Reranking** in RAG (Retrieval-Augmented Generation) pipelines — covering concepts, techniques, diagrams, code snippets, and comparisons.


---

## 📂 Files

| File | Description |
|------|-------------|
| `reranking_poster.png` | Exported PNG image (1060 × 3311 px) |
| `README.md` | This file |

---

## 📖 What's Covered

The poster walks through the following topics:

### 1. RAG Pipeline Overview
- Step 1: Initial Retrieval (Vector Search / BM25)
- Step 2: Reranking
- Output: Top-K Relevant Chunks → LLM Generation

### 2. Why Reranking Matters
- Precision, Noise Reduction, Context Quality
- Reduced Hallucination, Cost Efficiency

### 3. Top 5 Reranking Techniques
| Technique | Description |
|-----------|-------------|
| **Cross-Encoder Reranking** | Deep neural scoring of query-document pairs |
| **Reciprocal Rank Fusion (RRF)** | Combines rankings from multiple retrievers |
| **Cohere Rerank API** | Managed, multilingual reranking service |
| **ColBERT (Late Interaction)** | Token-level MaxSim similarity |
| **LLM-as-a-Judge** | LLM evaluates and scores relevance |

### 4. Deep Dives
- **Cross-Encoder** — architecture diagram, when to use, example query
- **RRF** — formula (`score = Σ 1/(k + rankᵢ)`), hybrid search use case
- **Cohere Rerank** — API diagram + Python code snippet
- **ColBERT** — token embedding grid, MaxSim interaction visual
- **LLM-as-a-Judge** — trade-offs, explainability, high-stakes use cases

### 5. Implementation Flow (Cross-Encoder)
Load Model → Define Query → Run Retrieval → Build Pairs → Score → Sort → Filter → Pass to LLM

### 6. Technique Comparison Table
Compares all 5 methods across **Accuracy**, **Speed**, and **Cost**.

---


## 🧠 Key Takeaway

> Reranking is the **quality gate** between retrieval and generation —
> the difference between a good RAG system and a great one.

Choose your technique based on: **Accuracy · Speed · Cost · Infrastructure**

---

## 📚 Further Reading

- [Cohere Rerank Docs](https://docs.cohere.com/docs/reranking)
- [ColBERT Paper (Stanford)](https://arxiv.org/abs/2004.12832)
- [Reciprocal Rank Fusion (RRF)](https://plg.uwaterloo.ca/~gvcormac/cormacksigir09-rrf.pdf)
- [Cross-Encoders — Sentence Transformers](https://www.sbert.net/examples/applications/cross-encoder/README.html)
- [LLM-as-a-Judge Survey](https://arxiv.org/abs/2306.05685)
