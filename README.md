# 🎯 Aspect-Based Sentiment Analysis (ABSA) using Transformers

An end-to-end NLP system that performs **fine-grained sentiment analysis** by identifying specific aspects in text (e.g., acting, plot, cinematography) and assigning sentiment to each.

---

## 🚀 Overview

Traditional sentiment analysis gives a single label (positive/negative), but real-world data contains **multiple opinions in a single review**.

This project builds an **Aspect-Based Sentiment Analysis (ABSA)** pipeline using transformer models to:
- Extract meaningful aspects from text
- Assign sentiment to each aspect
- Enable detailed, interpretable insights

---

## 🧠 Key Features

- 🔍 **Semantic Aspect Extraction** using Sentence-BERT (all-MiniLM-L6-v2)
- 🏷️ **Weak Supervision Labeling** using DistilBERT (SST-2)
- 🤖 **Fine-tuned BERT Classifier** for sentiment prediction
- ⚡ **High Accuracy:** 94.28% on IMDB dataset
- 📊 Processes **25K+ reviews & 24K+ aspect-level samples**
- 🎯 Supports **real-time, high-confidence inference (99%+)**

---

## 🏗️ Architecture


Raw Reviews
↓
Sentence Segmentation
↓
Aspect Extraction (Sentence-BERT + Cosine Similarity)
↓
Weak Labeling (DistilBERT)
↓
Dataset Creation (Aspect-Level)
↓
BERT Fine-Tuning
↓
Aspect-wise Sentiment Output


---

## 📂 Dataset

- **IMDB 50K Movie Reviews Dataset**
- Balanced dataset with positive and negative reviews
- Converted into **aspect-level labeled dataset**

---

## ⚙️ Tech Stack

- Python
- PyTorch
- HuggingFace Transformers
- Sentence-BERT
- Scikit-learn
- NumPy / Pandas

---

## 📈 Model Details

- **Base Model:** BERT
- **Labeling Model:** DistilBERT (SST-2)
- **Embedding Model:** Sentence-BERT
- Techniques used:
  - Class weighting (handles imbalance)
  - Dropout (0.3)
  - Gradient clipping
  - Learning rate scheduling

---

## 📊 Results

| Metric        | Score   |
|--------------|--------|
| Accuracy     | 94.28% |
| Precision    | High   |
| Recall       | High   |
| Confidence   | 99%+   |

---

## 🧪 Example

**Input:**

"The acting was amazing but the story was boring."


**Output:**

Acting → Positive
Story → Negative
