# 📖 Book Recommendation System

This project is a **Content-Based Book Recommendation System** built using **Python** and **Scikit-learn**, developed as part of the **Machine Learning with Python course** by [freeCodeCamp.org](https://www.freecodecamp.org/). The system recommends books based on user rating similarities using a k-Nearest Neighbors (k-NN) model.

---

## 🔍 Project Overview

The goal of this project is to suggest similar books based on a selected title by analyzing user ratings. The system uses **collaborative filtering** with cosine similarity to find books that were liked by users who also liked the given book.

---

## 📦 Dataset

The dataset used is the [Book-Crossing Dataset](http://www2.informatik.uni-freiburg.de/~cziegler/BX/), which includes:

- `BX-Books.csv` – metadata about books
- `BX-Book-Ratings.csv` – user ratings for books

The files are downloaded and unzipped automatically inside the notebook.

---

## 🧠 Techniques and Libraries

- **Pandas** for data manipulation
- **NumPy** for numerical operations
- **Scikit-learn** for machine learning (k-Nearest Neighbors)
- **Matplotlib** for optional plotting
- **CSR Matrix** (from `scipy`) for memory-efficient sparse matrices

---

## 🛠️ How It Works

1. **Filter active users and popular books** to reduce data size.
2. **Merge books and ratings** into a single DataFrame.
3. **Create a pivot table** of users and books.
4. **Convert to a sparse matrix** to optimize performance.
5. **Train a NearestNeighbors model** using cosine similarity.
6. **Define a function `get_recommends(book)`** that:
   - Takes a book title as input.
   - Finds top 5 similar books based on ratings.
   - Returns the recommended titles and similarity scores.

---

## 🚀 How to Run

1. Open the project notebook in **Google Colab** (recommended).
2. Run each cell in order.
3. Use the `get_recommends("Book Title")` function to see recommendations.

📎 [Open in Google Colab](https://colab.research.google.com/) *(replace with your notebook link)*

---

## ✅ Sample Output

```python
get_recommends("Where the Heart Is (Oprah's Book Club (Paperback))")

# Output:
[
  "Where the Heart Is (Oprah's Book Club (Paperback))",
  [
    ["I'll Be Seeing You", 0.8001],
    ["The Weight of Water", 0.7723],
    ["The Surgeon", 0.7690],
    ["I Know This Much Is True", 0.7685],
    ["The Lovely Bones", 0.7543]
  ]
]
