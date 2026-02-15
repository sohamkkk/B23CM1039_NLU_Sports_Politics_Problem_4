# Sports vs Politics Text Classification

## Overview

This documents a binary text classification system for distinguishing between sports and politics news articles. The paper is based on the Jupyter notebook implementation and provides an academic-level analysis of the methodology, experiments, and results.

## Document Structure

### 1. **Title Page and Abstract**
- Professional title page with document metadata
- Comprehensive abstract summarizing the research
- Keywords for academic indexing

### 2. **Table of Contents**
- Detailed table of contents with section numbering
- List of figures
- List of tables

### 2. **Problem Statement**

### 3. **Data Collection and Analysis**
- Dataset source (Kaggle News Category Dataset)
- Dataset characteristics (10,000 articles, perfectly balanced)
- Data filtering and preparation
- Text feature construction
- Exploratory data analysis with visualizations

### 6. **Methodology (Section 4)**
- **Text Preprocessing**: Cleaning, lowercasing, special character removal
- **Feature Extraction**: 
  - Bag of Words (BoW)
  - TF-IDF
  - TF-IDF with N-grams
- **Train-Test Split**: 80-20 split with stratification
- **Machine Learning Algorithms**:
  - Naive Bayes (Multinomial)
  - Logistic Regression
  - Support Vector Machines (Linear SVM)
  - K-Nearest Neighbors (KNN)
  - Random Forest
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1-Score, Confusion Matrix

### 7. **Experimental Results (Section 5)**
- Overall performance comparison across 15 configurations
- Detailed results for each feature type
- Confusion matrix analysis
- Learning curves
- Runtime analysis

### 9. **Conclusion**
- Summary of contributions
- Performance achievements
- Practical implications

### 10. **References**
- Academic citations for methods and datasets used

### 11. **Appendices**
- Complete code implementation
- Hardware and software specifications
- Additional experimental results

## Key Results

### Best Performing Model
- **Algorithm**: Linear Support Vector Machine (SVM)
- **Features**: TF-IDF with N-grams (unigrams + bigrams)
- **Accuracy**: **98.25%**
- **Precision**: 0.98
- **Recall**: 0.98
- **F1-Score**: 0.98

### Performance Summary

| Classifier           | BoW     | TF-IDF  | TF-IDF + N-grams |
|---------------------|---------|---------|------------------|
| Naive Bayes         | 97.25%  | 97.65%  | 97.15%           |
| Logistic Regression | 97.85%  | 98.10%  | 98.10%           |
| Linear SVM          | 97.80%  | 98.05%  | **98.25%**       |
| K-Nearest Neighbors | 91.95%  | 93.15%  | 93.80%           |
| Random Forest       | 96.55%  | 97.65%  | 97.15%           |

## Technical Details

### Dataset
- **Source**: Kaggle News Category Dataset
- **Total Articles**: 10,000 (5,000 Politics + 5,000 Sports)
- **Split**: 8,000 training / 2,000 testing (80-20)
- **Balance**: Perfectly balanced classes

### Features
- **Vocabulary Size**: 5,000 most frequent terms
- **Feature Types**: Word counts, TF-IDF scores, N-grams
- **Preprocessing**: Lowercase, special character removal, stop word removal

### Algorithms
All implemented using scikit-learn with default parameters (except where noted):
- Multinomial Naive Bayes
- Logistic Regression (max_iter=1000)
- Linear SVM
- KNN (k=5)
- Random Forest (n_estimators=200)

---
