# 🔍 Information Retrieval System using NLP

## 📌 Project Overview
This project implements a **classical Information Retrieval (IR) system** using **Natural Language Processing (NLP)** techniques on the **Cranfield dataset**.  
The system ranks documents for user queries using a **Query Likelihood Language Model with Jelinek–Mercer smoothing** and improves retrieval quality through **Rocchio relevance feedback**.

The project demonstrates practical understanding of **IR theory, probabilistic ranking models, relevance feedback mechanisms, and standard evaluation metrics** used in search engines.

---

## 📚 Dataset
- **Dataset:** Cranfield Collection
- **Source:** `ir_datasets`
- **Domain:** Aeronautical engineering document abstracts
- **Includes:**
  - Documents
  - Queries
  - Relevance judgments (qrels)

---

## 🧠 Methodology

### 1️⃣ Text Preprocessing
- Tokenization
- Lowercasing
- Stopword removal
- Term frequency computation

These steps convert raw text into structured representations suitable for retrieval models.

---

### 2️⃣ Query Likelihood Language Model
- Probabilistic ranking model
- Uses **Jelinek–Mercer smoothing** to handle unseen terms
- Ranks documents based on likelihood of generating the query

**Formula:**
P(q | d) = ∏ [ λ · P(w | d) + (1 − λ) · P(w | C) ]
---

### 3️⃣ Rocchio Relevance Feedback
- Improves query representation using pseudo-relevant documents
- Refines query vectors to enhance ranking quality

**Formula:**
q_new = αq + β(1/|Dr|)∑Dr − γ(1/|Dnr|)∑Dnr


---

## 📊 Evaluation Metrics
The system is evaluated using standard IR metrics:
- **Precision@K**
- **Mean Average Precision (MAP)**
- **Mean Reciprocal Rank (MRR)**

Evaluation is performed using official Cranfield relevance judgments.

---

## 🧪 Custom Query Support
- Supports user-defined natural language queries
- Displays ranked documents with relevance scores
- Automatically evaluates queries present in the dataset

---

## 📈 Key Insights
- Jelinek–Mercer smoothing improves robustness for short queries
- Rocchio feedback enhances early-rank precision
- Classical IR models remain effective without deep learning

---

## 🛠 Tech Stack
- **Language:** Python
- **Libraries & Tools:**
  - NLP preprocessing techniques
  - `ir_datasets`
  - NumPy
  - collections, math

---
