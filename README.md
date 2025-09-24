# 🗂️ Reddit NLP Project  
### By **Rubén Gil** & **Guille López**

This repository presents a complete **Natural Language Processing (NLP)** pipeline applied to **Reddit comments**, covering data collection, lexical processing, classification, semantic search, sentiment & emotion analysis, abstractive summarization, and inappropriate content detection.  

---

## 📥 Data Collection  
We compiled a **custom corpus of Reddit comments** using the official Reddit API.

- **6 different subreddits**  
- **20 threads per subreddit**  
- ~**50 comments per thread**  

The corpus was stored as **individual JSON files**, one per subreddit, to facilitate modular analysis.

---

## 🔤 Lexical Processing  
We used **spaCy** for comprehensive text processing and **SymSpellPy** for spelling correction.

### Preprocessing with spaCy
- Tokenization  
- Detection of numbers and punctuation  
- Stopword removal using spaCy’s built-in list  
- **Context-aware lemmatization** for more accurate word forms

### Spelling Correction
- **SymSpellPy** was used to efficiently detect and correct misspellings.

#### ✅ Advantages of spaCy
- Context-based lemmatization for irregular forms  
- Faster and more efficient than NLTK  
- Up-to-date language models optimized for modern text

---

## 🏗️ Key Components of the Project

### 1️⃣ Subreddit Comment Classification  
Classification of Reddit comments by topic using a variety of **tokenizers, vectorizers, and embeddings**.  
- Performed **GridSearch** and fine-tuning to identify the best-performing classifier.  
- Implemented **DistilBERT fine-tuning** for superior performance.

---

### 2️⃣ Similar Thread Search & Visualization  
Identification of **similar Reddit threads** using **sentence embeddings**.  
- **Dimensionality reduction with PCA** to visualize thread relationships in 2D space.  
- Enables exploration of semantic proximity between discussion threads.

---

### 3️⃣ Sentiment & Emotion Analysis  
Applied **pretrained models** to detect the sentiment and emotional tone of comments:  
- **Sentiment:** [`pysentimiento/robertuito-sentiment-analysis`](https://huggingface.co/pysentimiento/robertuito-sentiment-analysis)  
- **Emotion:** [`finiteautomata/beto-emotion-analysis`](https://huggingface.co/finiteautomata/beto-emotion-analysis)

---

### 4️⃣ Abstractive Summarization  
Generated **human-like, abstractive summaries** of Reddit threads.  
- Approach 1: Fine-tuned model specifically trained for summarization.  
- Approach 2: **Prompt engineering** to guide large language models (LLMs) for flexible text generation.

---

### 5️⃣ Inappropriate Content Detection  
Detection of **inappropriate or harmful content** using multiple strategies:
- **Zero-Shot Learning (ZSL)**
- **Few-Shot Learning (FSL)**
- **Chain-of-Thought reasoning** for improved model explainability.

---

## ⚙️ Tech Stack
- **Data Collection:** Reddit API, Python  
- **Processing & Modeling:** spaCy, SymSpellPy, scikit-learn, Transformers (Hugging Face)  
- **Visualization:** PCA, Matplotlib/Seaborn  
- **Pretrained Models:** DistilBERT, RoBERTuito, BETO, Gemma, mT5

---

## 🌟 Highlights
- End-to-end **data-to-insight pipeline** on real Reddit content.  
- Combination of **traditional NLP** (tokenization, lemmatization) with **modern transformer models**.  
- Integration of **classification, retrieval, sentiment/emotion analysis, summarization**, and **content moderation** within one cohesive framework.

---

## 📜 License
This project is released under the **MIT License**.  
Feel free to use, adapt, and build upon this work with proper attribution.

---

### 🙌 Authors
- **Rubén G.M**  
- **Guillermo L.P**
