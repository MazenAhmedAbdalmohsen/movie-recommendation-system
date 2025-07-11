# 🎬 Movie Recommendation System

This project builds a **hybrid movie recommendation system** using both collaborative filtering and content-based filtering. It leverages user ratings and movie metadata to suggest personalized movies.

## 📂 Dataset

The dataset is sourced from Kaggle:

- **Source**: [Movie Recommendation System Dataset](https://www.kaggle.com/datasets/parasharmanas/movie-recommendation-system)
- **Files**:
  - `movies.csv` – Movie metadata (title, genres)
  - `ratings.csv` – User ratings (userId, movieId, rating)

---

## 🔍 Features

✅ Collaborative Filtering using **SVD (Singular Value Decomposition)**  
✅ Content-Based Filtering using **TF-IDF Vectorization**  
✅ Hybrid recommender support  
✅ Saved models for deployment  
✅ Built for use in **Google Colab**

---

## 📦 Project Files

| File | Description |
|------|-------------|
| `Movie_Recommendation_System.ipynb` | Main notebook |
| `movie_recommender_svd_model.pkl` | Trained collaborative filtering model |
| `tfidf_matrix.pkl` | TF-IDF matrix of cleaned movie titles |
| `tfidf_vectorizer.pkl` | TF-IDF vectorizer fitted on movie titles |
| `README.md` | Project documentation |
| `requirements.txt` | Required dependencies |

---

## 🧠 Model Details

### 1. Collaborative Filtering (SVD)

- Library: `Surprise`
- Training data: `ratings.csv`
- Evaluation metric: RMSE
- Saved model: `movie_recommender_svd_model.pkl`

### 2. Content-Based Filtering (TF-IDF)

- Library: `sklearn`
- Input: `movies.csv['title']`
- Vectorizer: `TfidfVectorizer(stop_words='english')`
- Saved artifacts:
  - `tfidf_matrix.pkl`
  - `tfidf_vectorizer.pkl`

---

## 🧪 Usage Example

### Predict a Rating (Collaborative)

```python
from joblib import load
model = load("movie_recommender_svd_model.pkl")
model.predict(str(1), str(50))  # userId=1, movieId=50
