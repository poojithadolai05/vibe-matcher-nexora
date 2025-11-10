# 🎯 Vibe Matcher — Nexora AI Internship Prototype

> A hybrid **vibe-based fashion recommender system** built for the Nexora AI Internship.  
> Uses **TF-IDF embeddings**, **OpenAI’s text-embedding-ada-002**, and **cosine similarity**  
> to match products to mood-based queries like *“energetic urban chic.”*

---

## 💡 Overview

This notebook demonstrates a **vibe-driven recommendation engine** inspired by Nexora’s vision —  
_“Where Vibes Meet Fashion.”_

Given a user’s vibe query, it identifies top-3 fashion items that match the mood using:
- **TF-IDF embeddings (offline mode)**  
- or **OpenAI embeddings (`text-embedding-ada-002`)** when available.  

It includes **cosine similarity ranking**, **vibe-aware query expansion**, and **fallback logic**  
for unseen or ambiguous vibe inputs — forming the foundation of a scalable **AI-driven fashion discovery engine.**

---

## ✨ Features

- 🧺 **Mock fashion dataset** (10 products with vibe tags)  
- 🧠 **Hybrid TF-IDF + OpenAI embedding pipeline**  
- 🔍 **Cosine similarity ranking** for vibe-query matches  
- 🪄 **Query expansion** with vibe-aware synonyms  
- ⚡ **Evaluation metrics:** Precision@3, MRR, latency & radar plots  
- 🧩 **Fallback logic** for weak or missing matches  
- 🪶 **Reflection** with future steps (Pinecone, GPT-4o, feedback loops)

---

## ⚙️ How to Run

### Option 1 — Run on Google Colab (Recommended)
1. Open the notebook on **Google Colab**  
2. Run all cells in order  
3. (Optional) Add your OpenAI API key to enable semantic embeddings

```python
os.environ["OPENAI_API_KEY"] = "sk-yourkey"
```
> 💡 If no API key is provided, it runs in offline TF-IDF mode automatically.

## 🖥️ Option 2 — Local Setup

To run this project locally on your system:

```bash
git clone https://github.com/poojithadolai05/vibe-matcher-nexora.git
cd vibe-matcher-nexora
pip install -r requirements.txt
jupyter notebook Vibe_Matcher_Nexora.ipynb
```

### 🧩 Dependencies

The following Python libraries are required:

- `pandas`  
- `numpy`  
- `matplotlib`  
- `scikit-learn`  
- `openai` *(optional — for semantic embedding mode)*  

> 💡 **Tip:** If you don’t provide an OpenAI API key, the notebook will automatically fall back to offline **TF-IDF mode**.

## 📊 Sample Output (Offline Mode)

| Query | Top Match | Quality | Latency (ms) |
|-------|------------|----------|--------------|
| energetic urban chic | Urban Denim Jacket | good | ~7 |
| soft cozy neutral home wear | Cozy Knit Sweater | good | ~10 |
| elegant evening dinner outfit | Silk Slip Dress | good | ~11 |

**Precision@3:** 1.00 | **MRR:** 1.00 | **Mode:** TF-IDF Boosted


## 🧭 Reflection & Next Steps

- **Hybrid design:** TF-IDF + optional OpenAI embeddings  
- **Query expansion + fallback:** improves robustness for vague queries  
- **Logged metrics:** quality, latency, and evaluation results  

### 🔮 Next Steps
- Integrate **Pinecone / FAISS** for scalable vector search  
- Add **feedback loops** for adaptive re-ranking  
- Prototype **GPT-4o-based vibe rewriting** for vague or creative prompts  

