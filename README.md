# Movie-Recommendation-System

## Overview

This project builds a recommendation system using collaborative filtering techniques on the **MovieLens 100K** dataset. The system recommends top-rated, unseen movies for a user by computing similarity scores and evaluates the performance using **Precision@K**.

---

## Dataset
- **Source:** [MovieLens 100K Dataset](https://www.kaggle.com/datasets/prajitdatta/movielens-100k-dataset)
- **Files Used:**
  - `u.data` → user ratings
  - `u.item` → movie metadata (titles)

## Tools & Libraries
- Python
- `pandas`, `numpy`
- `scikit-learn`
- `matplotlib`, `seaborn`

## Objective
- Build a movie recommendation system using collaborative filtering.
- Compute similarity scores using cosine similarity.
- Recommend top-rated unseen movies to users.
- Evaluate recommendations using **Precision@K**.
- Bonus: Implement Item-based and SVD-based (Matrix Factorization) approaches.

## Key Steps & Results
### Feature Engineering
- Created a **user-item rating matrix** (users as rows, movie titles as columns).
- Missing ratings are filled with `0` to prepare for similarity calculations.

### User-Based Collaborative Filtering
- Cosine similarity between users based on their ratings.
- Recommend items that **similar users** liked but the current user hasn't seen.

### Item-Based Collaborative Filtering (Bonus)
- Cosine similarity between items based on user ratings.
- Recommend items **similar to those** the user has already liked.

### Matrix Factorization with SVD (Bonus)
- Applied **Truncated SVD** to decompose the user-item matrix into latent features.
- Reconstructed the matrix and recommended top-rated unseen items.

### Evaluation with Precision@10
For a sample user (e.g., `user_id = 5`), the model computes:
- Precision@10 (User-based): 0.3
- Precision@10 (Item-based): 0.2
- Precision@10 (SVD):        0.4
