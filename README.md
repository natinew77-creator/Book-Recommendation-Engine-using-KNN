# Book Recommendation Engine (K-Nearest Neighbors)

## Project Overview
This project involves building a collaborative filtering recommendation system using the K-Nearest Neighbors (KNN) algorithm. The goal was to accurately find similar books based on user ratings. This challenge was completed as part of the freeCodeCamp Machine Learning with Python Certification.

* **Key Challenge:** Rigorous data cleaning was required on a dataset of over 1.1 million ratings to reduce noise.
* **Final Result:** Passed all hidden test cases.

---

## Model Architecture & Data Handling

The effectiveness of this model relies on preparing the highly sparse (mostly empty) dataset correctly.

### Key Techniques:

* **Data Filtering:** Removed all users who rated less than **200 books** and all books that received less than **100 ratings**.
* **Matrix Creation:** Transformed the data into a large, dense matrix using a **Pivot Table** (Index=Title, Columns=User, Values=Rating).
* **Sparsity:** Converted the matrix into a **CSR (Compressed Sparse Row) matrix** to efficiently handle the memory usage.
* **Algorithm:** Used the `NearestNeighbors` model from `sklearn` with **`metric='cosine'`** to calculate similarity between books.
* **Output Format:** Successfully implemented the required logic to return the recommendation list in the specific reversed format expected by the test cases.

---

## 🔗 Live Code & Execution

Click the link below to view the executable Google Colab notebook.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/10u4CvuNgz8vqWM-v_cBFIF8huwzDw4EC?usp=sharing)
