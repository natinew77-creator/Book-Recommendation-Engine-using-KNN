# Book Recommendation Engine (K-Nearest Neighbors)

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)](https://scikit-learn.org/stable/)
[![Pandas](https://img.shields.io/badge/Library-Pandas-150458)](https://pandas.pydata.org/)
![Status](https://img.shields.io/badge/Status-Completed-success)](https://github.com/natinew77-creator/Book-Recommendation-Engine-using-KNN/blob/main/README.md#results--performance)

## 📌 Project Overview
This project is a robust **Collaborative Filtering Recommendation System** built to suggest books based on user rating patterns. By analyzing over **1.1 million ratings**, the system identifies semantic similarities between books without needing to know the content (genre, author, etc.) of the books themselves.

Developed as part of the **FreeCodeCamp Machine Learning with Python Certification**, this solution demonstrates the practical application of unsupervised learning algorithms to solve real-world information retrieval problems.

---

## 🚀 Key Technical Achievements

### 1. High-Volume Data Processing & Cleaning
Handling a dataset of this magnitude requires rigorous preprocessing to ensure model reliability.
*   **Statistical Filtering:** Implemented logic to filter out noise by removing users with fewer than **200 ratings** and books with fewer than **100 ratings**. This ensures the model learns only from active users and well-established items.
*   **Data Integrity:** Merged multiple CSV datasets (Books, Ratings, Users) while handling encoding issues (`ISO-8859-1`) and missing values.

### 2. Memory Optimization with Sparse Matrices
A common challenge in recommendation systems is the "sparsity" of the data (most users haven't read most books).
*   **Pivot Table Transformation:** Converted the dataset into a 2D matrix (Index: Book Title, Columns: User ID, Values: Rating).
*   **CSR Implementation:** Transformed the dense matrix into a **SciPy Compressed Sparse Row (CSR) matrix**. This drastically reduced memory usage and improved computational efficiency during model training.

### 3. Unsupervised Learning Implementation
*   **Algorithm:** Utilized the **K-Nearest Neighbors (KNN)** algorithm (`sklearn.neighbors.NearestNeighbors`).
*   **Metric:** Employed **Cosine Similarity** to measure the distance between book vectors. Unlike Euclidean distance, Cosine similarity focuses on the orientation of the vectors, making it ideal for rating data where the magnitude (number of ratings) might differ but the pattern is similar.

---

## 🛠️ Technologies Used

*   **Language:** Python 3
*   **Machine Learning:** Scikit-Learn (NearestNeighbors)
*   **Data Manipulation:** Pandas, NumPy
*   **Scientific Computing:** SciPy (Sparse Matrices)
*   **Visualization:** Matplotlib

---

## 📊 Results & Performance

The model was validated against a strict testing suite to ensure accuracy.

**Example Inference:**
When querying for the book **"Where the Heart Is (Oprah's Book Club (Paperback))"**, the model successfully returns the following recommendations based on user affinity:

1.  *I'll Be Seeing You* (Distance: 0.80)
2.  *The Weight of Water* (Distance: 0.77)
3.  *The Surgeon* (Distance: 0.77)
4.  *I Know This Much Is True* (Distance: 0.77)
5.  *The Lovely Bones: A Novel* (Distance: 0.72)

**Outcome:** Passed all automated test cases with 100% accuracy.

---

## � How to Run

You can view and execute the code directly in Google Colab, or run it locally.

### Option 1: Google Colab (Recommended)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/10u4CvuNgz8vqWM-v_cBFIF8huwzDw4EC?usp=sharing)

### Option 2: Local Installation
1.  Clone the repository.
2.  Install dependencies:
    ```bash
    pip install pandas numpy scikit-learn scipy matplotlib
    ```
3.  Run the Jupyter Notebook:
    ```bash
    jupyter notebook Copy_of_fcc_book_recommendation_knn.ipynb
    ```

---

## 👨‍💻 Author
**Natneal B.**  
*Machine Learning Engineer & Developer*
