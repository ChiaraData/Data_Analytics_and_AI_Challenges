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
*Developed by Chiara Masi, student number : 909059*
