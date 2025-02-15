# Intelligent Candidate Ranking System

## Project Summary

This project automates candidate sourcing and ranking for a talent management company. It aims to accurately interpret client requirements, evaluate candidate fitness, and improve rankings based on human feedback (e.g., starring). The system continuously adapts to align with reviewer preferences.

## Key Features

- **Fitness Prediction & Ranking:**  
  Calculate candidate fitness scores and rank candidates accordingly.

- **Re-ranking with Feedback:**  
  Update rankings using human feedback (starred candidates).

- **Filtering & Adaptive Cut-off:**  
  Automatically filter out low-potential candidates using a dynamic threshold.

- **Bias Mitigation:**  
  Integrate techniques to minimize human bias during evaluation.

## Techniques Used

- **Text Embedding:**  
  - Word2Vec  
  - BERT  
  - fastText  
  - GloVe

- **Similarity & Retrieval:**  
  Cosine similarity and retrieval-based methods for initial candidate matching.

- **Learning-to-Rank:**  
  - **RankNet:** Uses pairwise comparisons and binary cross-entropy loss.  
  - **LambdaRank:** Enhances RankNet by incorporating changes in ranking metrics (e.g., NDCG) directly into the training process.

## Data Description

The dataset contains anonymized candidate information with the following attributes:
- **id:** Unique candidate identifier.
- **job_title:** Candidate's job title.
- **location:** Geographical location.
- **connections:** Number of professional connections.
- **fit:** (Target) Fitness score, computed using cosine similarity and text embeddings.

## Goals & Objectives

- Develop a predictive model to calculate fitness scores.
- Rank and re-rank candidates based on computed scores and human feedback.
- Integrate multiple NLP techniques for enhanced candidate matching.
- Streamline the talent sourcing process while reducing manual effort and bias.
