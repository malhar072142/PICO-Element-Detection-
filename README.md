# **Automated PICO Element Detection for Biomedical Literature**

## **Introduction**
The **evidence-based medicine (EBM)** approach relies on integrating findings from randomized controlled trials (RCTs) into clinical decision-making. This project aims to **automate PICO element detection** in medical literature using deep learning models, improving literature retrieval and analysis for clinical research.

The **PICO framework** breaks down clinical questions into four key components:
- **P**articipants/Problem
- **I**ntervention
- **C**omparison
- **O**utcome

Since many biomedical abstracts lack clear PICO labeling, this project focuses on automating their classification using **Natural Language Processing (NLP)** techniques.

---

## **Project Workflow**
### **1. Dataset Collection & Preprocessing**
- Used **PubMed PICO Element Detection Dataset** from randomized controlled trials (RCTs).
- Applied **text cleaning, tokenization, and embedding generation**.
- Explored custom **Word2Vec, GloVe, and FastText embeddings**.

### **2. Exploratory Data Analysis (EDA)**
- Visualized PICO element distribution.
- Analyzed sentence lengths, word frequency, and PICO co-occurrence patterns.

### **3. Feature Engineering**
- Mapped **PICO elements** to numerical classes.
- Converted text data into word embeddings using **Word2Vec**.
- Applied **padding** and **one-hot encoding** for model input structuring.

### **4. Model Training & Evaluation**
- **Baseline Model:** Logistic Regression with TF-IDF (**Accuracy: 27.3%**).
- **Deep Learning Models:**
  - **Feedforward Neural Network (FFNN)** (**Accuracy: 29.1%**)
  - **BiLSTM with Attention** (**Accuracy: 77.74%**)
  - **BERT** (**Accuracy: 84.2%**)
  - **DistilBERT (Knowledge Distillation)** (**Accuracy: 84.43%**) → Best model!

### **5. Final Model Deployment**
- **DistilBERT was selected** for its high accuracy and computational efficiency.
- Model trained for **PICO element classification** in medical abstracts.


## **Dataset & Model Checkpoints**

## Dataset

- Source: MEDLINE abstracts from PubMed
- Total Abstracts: 489,026
- Analyzed Abstracts: 24,668 (containing P, I, O labels)
- Domain: Randomized Controlled Trials (RCTs)

The dataset and trained model checkpoints are available in the following Google Drive folder:

📂 **Google Drive Link:** [Click Here](https://drive.google.com/drive/folders/1ijYrBCr-7F8jUoqKVYBUS6SbpXeODG1v?usp=drive_link)

Download the files and place them in the respective directories before running the model.

---

## Project Overview

This research project develops an advanced machine learning solution for automatically detecting and classifying PICO (Participants/Problem, Intervention, Comparison, Outcome) elements in biomedical research abstracts. By leveraging state-of-the-art natural language processing techniques, the project aims to streamline evidence-based medicine (EBM) research by automating the extraction of critical study components.

## Key Features

- Automated detection of PICO elements in medical literature
- Multiple model implementations, including:
  - Logistic Regression with TF-IDF
  - Feed-Forward Neural Network (FFNN)
  - Bidirectional LSTM with Attention
  - BERT and DistilBERT models
- Comprehensive word embedding techniques:
  - Custom Word2Vec
  - GloVe Embeddings
  - FastText Embeddings
- Knowledge distillation for model efficiency

## Performance Metrics

| Model | Accuracy | Key Characteristics |
|-------|----------|---------------------|
| DistilBERT | 84.43% | Most efficient, near-BERT performance |
| BERT | 84.20% | Highest contextual understanding |
| BiLSTM with Attention | 77.74% | Strong sequential dependency capture |
| FFNN | 29.10% | Basic neural network approach |
| Logistic Regression | 27.30% | Baseline model |


## Research Highlights

- Developed custom Word2Vec embeddings for biomedical text
- Implemented advanced NLP models for complex text classification
- Achieved high accuracy in detecting research paper components
- Demonstrated effectiveness of knowledge distillation