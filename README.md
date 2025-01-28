# **Sentiment Analysis Using BERT and Lexicon-Based K-NN Approach**  

This project implements **sentiment analysis** by leveraging **BERT embeddings** (both **contextual** and **non-contextual**) and a **lexicon-based K-Nearest Neighbors (K-NN) approach**. The goal is to classify the sentiment of input text based on word embeddings and predefined sentiment labels from a lexicon.  

## 🚀 **Project Overview**  
- **Embedding Extraction**:  
  - **Contextual Embeddings**: Extracted from BERT’s last hidden state, capturing word meanings based on surrounding words.  
  - **Non-Contextual Embeddings**: Extracted from BERT’s `word_embeddings` layer, representing words independently.  
- **Lexicon-Based Sentiment Matching**:  
  - A precomputed **sentiment lexicon** (`filtered_lexicon.csv`) contains words with associated **priorpolarity** (positive, negative, neutral).  
  - **Cosine Similarity & K-NN** are used to find the closest matching words in the lexicon.  
  - The most frequent sentiment among the top-K matches is assigned.  
- **User Input Classification**:  
  - The model allows **real-time user input**, computes embeddings, and assigns sentiment dynamically.  

## 🔧 **How It Works**  
1. **Dataset Preprocessing**:  
   - Loads a filtered dataset (`dataset_filtered.csv`).  
   - Cleans text by removing URLs, mentions, and special characters.  
   - Tokenizes sentences using **BERT tokenizer**.  
2. **Embedding Computation**:  
   - **Contextual embeddings** are extracted from `last_hidden_state`.  
   - **Non-contextual embeddings** are extracted from `word_embeddings`.  
3. **Sentiment Assignment with K-NN**:  
   - Finds the **K nearest neighbors** in the lexicon using **cosine similarity**.  
   - Assigns the **most frequent sentiment** among top-K matches.  
4. **Evaluation & User Testing**:  
   - The model is tested on predefined datasets and allows **user input for live predictions**.  



