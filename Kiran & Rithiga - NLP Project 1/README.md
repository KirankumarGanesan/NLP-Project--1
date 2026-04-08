# NLP Evaluation Model: BM25 vs. TF-IDF

This project evaluates the performance of different Information Retrieval models (BM25 and TF-IDF) in recommending points of interest based on TripAdvisor review data.

## 👥 Team Members
* **Kiran Kumar GANESAN**
* **Rithiga VENGADESSANE**

## 📊 Project Overview
The core objective of this project is to measure "Ranking Error" across two levels of specificity:
* **Level 1:** General category matching (e.g., matching a Restaurant to a Restaurant).
* **Level 2:** Specific sub-category/cuisine matching.

### **Key Findings**
The TF-IDF model significantly outperformed the BM25 baseline in specific detail matching, reducing Level 2 error by **68.7%**.

---

## 📁 Dataset & Repository Structure
To keep this repository lightweight and adhere to GitHub's file size limits, the primary dataset has been excluded from the remote repository.

* **`Kiran Rithiga NLP Evaluation Model.ipynb`**: The main notebook containing data cleaning, model implementation, and evaluation loops.
* **`Dataset/`**: Contains metadata files such as `Tripadvisor.csv`, `cuisine.csv`, and `restaurantType.csv`.
* **`.gitignore`**: Configured to ignore large binary/CSV files and Jupyter checkpoints.

### **⚠️ Missing File: `reviews83325.csv`**
The file `reviews83325.csv` (approx. 210 MB) is required to run the notebook.
* **Why it's missing:** GitHub limits individual file uploads to 100 MB.
* **How to run locally:** Please ensure the `reviews83325.csv` file is placed in the `Dataset/` folder before executing the notebook cells.

---

## 🚀 Technical Implementation
The project utilizes the following stack:
* **NLP Libraries:** `nltk`, `rank-bm25`.
* **Machine Learning:** `scikit-learn` (`TfidfVectorizer`, `cosine_similarity`).
* **Data Processing:** `pandas`, `numpy`.

---

### **Final Project Performance Dashboard**
| Metric | BM25 (Baseline) | TF-IDF (Adv Model) |
| :--- | :--- | :--- |
| **Level 1 Error** | 1.08 | 0.86 |
| **Level 2 Error** | 56.62 | 17.75 |
