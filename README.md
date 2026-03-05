# Data Analytics and Artificial Intelligence - Master's Challenges

This repository contains a series of projects and challenges developed as part of the **Data Analytics and Artificial Intelligence** course during my **Master’s in Data Analytics for Business and Society** at **Ca' Foscari University of Venice**.

## 📚 Challenge 1: ML Book Recommender System
The goal of this challenge was to design a professional recommendation engine for an online marketplace.Using a real-world dataset of 500 books from OpenLibrary.org, I built a pipeline that cleans raw data and ranks titles based on technical relevance.

### Key Implementation Details:
* **Data Cleaning & Enrichment**: 
    * Performed duplicate removal and handled missing values. 
    * Manually researched and filled missing publication dates to ensure high data quality.
    * Applied an ASCII-ratio heuristic (80%) to filter for English-language titles.
* **Scoring Methodology**: 
    * Developed a weighted scoring system: **50% for Recency**, **30% for Popularity (Editions)**, and **20% for Python relevance**.
    * Used logarithmic normalization for edition counts to balance the influence of "classics" versus modern technical books.
* **Tie-Breaking Logic**: Implemented a secondary sorting rule based on edition counts and alphabetical order for consistent rankings.
---
## 🔢 Challenge 2: Unsupervised Optical Character Recognizer (OCR)
The goal of this challenge was to build an unsupervised OCR system using the NIST handwritten digits dataset (1,797 samples, 64 features). Without using any labels during training, I clustered digit images and evaluated how well clustering alone can recover digit identity.

### Key Implementation Details:
* **Clustering Methods**:
    * Applied **K-Means** (k=10, n_init=20) and **Agglomerative Clustering** (Ward linkage, k=10).
    * Visualised K-Means centroids and Agglomerative pseudo-centroids, medoids, and dendrograms to inspect cluster structure.
* **Cluster–Label Alignment**:
    * Since cluster IDs are arbitrary, used the **Hungarian algorithm** (scipy.optimize.linear_sum_assignment) to find the optimal bijective mapping between cluster IDs and true digit labels.
    * This approach maximises overall accuracy without any supervision.
* **Evaluation**:
    * K-Means reached **79.4% accuracy** — digit 0 was best recovered (99%), digit 1 was hardest (30%).
    * Agglomerative Clustering reached **84.0% accuracy** — digit 0 perfect (100%), digit 9 was hardest (11%).
    * Analysed confusion matrices and misclassification examples to explain why visually similar digits (1↔8, 3↔8, 4↔9, 5↔6) are harder to separate in raw 8×8 pixel space.

---
*Developed by Chiara Masi, student number : 909059*
