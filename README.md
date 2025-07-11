# 🎬 Movie Recommendation System

This project builds a movie recommendation system using the [Movie Recommendation System dataset on Kaggle](https://www.kaggle.com/datasets/parasharmanas/movie-recommendation-system). It uses collaborative filtering (SVD algorithm from Surprise library) to recommend personalized movie suggestions based on user ratings.

## 📁 Dataset

The dataset contains two main files:

- **movies.csv**: Contains movie metadata (movieId, title, genres).
- **ratings.csv**: Contains user ratings for movies (userId, movieId, rating, timestamp).

Dataset link: [Kaggle - Movie Recommendation System](https://www.kaggle.com/datasets/parasharmanas/movie-recommendation-system)

## 🚀 Features

- Clean and explore movies and ratings data.
- Build collaborative filtering model using the SVD algorithm.
- Train/test split for model evaluation.
- Calculate RMSE for performance.
- Generate top-N recommendations for a specific user.
- Save and load trained model using `joblib`.
- Ready for deployment or integration into a movie platform.

## 🧠 Model

The model is built using the **Surprise** library:

- Algorithm: `SVD` (Singular Value Decomposition)
- Metric: `RMSE` (Root Mean Square Error)
- Saved model file: `svd_movie_recommender.pkl`

## 📝 How to Use in Google Colab

1. Upload your `kaggle.json` to authenticate Kaggle API.
2. Run the notebook: `Movie_Recommendation_System.ipynb`.
3. Train the model and generate movie recommendations.
4. Use the saved model (`svd_movie_recommender.pkl`) for inference.

## 💻 Key Notebooks

- **Movie_Recommendation_System.ipynb**: Main notebook for training, evaluation, and generating recommendations.

## 📦 Dependencies

Install required libraries:
```bash
pip install scikit-surprise kaggle
