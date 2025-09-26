# Geo-Aware Text Summarization with NLP and Transformers

## 📌 Overview
This project implements a text summarization pipeline using **T5 Transformer** (abstractive) and **TextRank** (extractive) methods. Additionally, it extracts **geographical locations** from text using **SpaCy + Geopy** to make the summaries more contextual. Evaluation is done using **ROUGE metrics**.

---

## 🚀 Features
- Abstractive summarization with **T5**.
- Extractive summarization with **TextRank**.
- Location extraction using **SpaCy NER + Geopy**.
- ROUGE-based evaluation for summary quality.
- Google Colab-friendly implementation.

---

## 🛠️ Installation
Run the following in Google Colab or your terminal:

```bash
pip install pandas spacy geopy transformers sumy rouge-score torch sentencepiece
python -m spacy download en_core_web_sm
📂 Project Workflow
Load dataset (CSV/Excel with articles).

Run summarization using:

TextRank (textrank_summary)

T5 Transformer (process_article)

Extract locations with SpaCy + Geopy (extract_locations).

Evaluate using ROUGE scores.

📊 Example Usage
python
Copy code
from summarizer import process_article, textrank_summary, extract_locations

article = "India is set to host the G20 summit in New Delhi with leaders from across the globe."
print("T5 Summary:", process_article(article, method="t5"))
print("TextRank Summary:", textrank_summary(article))
print("Locations:", extract_locations(article))
✅ Results
T5 generates fluent summaries.

TextRank extracts key sentences.

Locations (like India, New Delhi) are extracted accurately.

ROUGE confirms the effectiveness of abstractive summarization.

📌 Applications
News summarization with geo-context.

Event monitoring systems.

Education & research support.

Geo-tagged insights from large text datasets.

👩‍💻 Author
Pallavi Meesala
Final Year Project (AI & NLP)
