# Reddit Comment Relevance Analysis: Rating Comments on a Scale of 1–5  

## 📌 Overview  
**Problem**  
Reddit discussions often accumulate hundreds of comments, but many lack relevance to the original post. This project automatically rates comments on a **1–5 relevance scale** to address information overload and improve content moderation.  

**Impact**  
- Helps users focus on meaningful discussions  
- Streamlines moderation efforts  
- Enhances community engagement by surfacing high-quality content  

## 🛠️ Tools  
**Languages & Frameworks**  
![Python 3.10.12](https://img.shields.io/badge/Python-3.10.12-blue?logo=python)  
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.12-orange?logo=tensorflow)  

**Key Libraries**  
![Pandas](https://img.shields.io/badge/Pandas-2.0-blueviolet?logo=pandas)  
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.2-grey?logo=scikit-learn)  
![HuggingFace](https://img.shields.io/badge/Transformers-4.30-yellow?logo=huggingface)  
![NLTK](https://img.shields.io/badge/NLTK-3.8-green)  

**ML Models (LLMs)**  
![BERT](https://img.shields.io/badge/BERT-uncased-ff69b4)  
![MiniLM](https://img.shields.io/badge/MiniLM-L6-violet)  
![LDA](https://img.shields.io/badge/LDA-Gensim-red)

## 🔍 Approach  
1. **Data Collection**  
   - Used Reddit API to gather 10 posts with moderate comment engagement (limited by API restrictions).  
2. **Preprocessing**  
   - Removed spam, URLs, emojis, and deleted comments  
   - Applied TF-IDF vectorization to posts/comments  
3. **Embedding Hybridization**  
   - Combined **LDA** (topic modeling) with **MiniLM/BERT** (semantic embeddings)  
4. **Clustering**  
   - KMeans clustering into 5 groups (1–5 relevance scale)  
5. **Relevance Scoring**  
   - Custom metric

## 📊 Results  
**Key Achievements**:  
- Hybrid models (LDA + MiniLM) achieved **clearer cluster separation** than standalone models  
- Example output for post *"Best iPhone 15 Pro Max color?"*:  
- **Cluster 2 (Score: 1.0)**: High-quality responses like *"I got white – fingerprints barely visible"*  
- **Cluster 0 (Score: 0.0)**: Irrelevant/spam comments  

