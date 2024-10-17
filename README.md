# BeerAdvocate Recommender System

## Description
This project was completed in 2023 as part of my exploration of recommendation systems and machine learning techniques using Python. The goal was to develop a recommender system for the BeerAdvocate platform, where users review and rate beers. The system uses **Collaborative Filtering** techniques to suggest beers based on user preferences and ratings.

## Objectives
- Build a recommender system to suggest personalized beer recommendations to users.
- Use **Collaborative Filtering** to predict user preferences based on similar users.
- Apply **K-Means algorithm** to group users in different clusters.

## Key Steps

### Data Cleaning and Preparation:
- Analyzed a dataset containing over 1.5 million reviews, focusing on key features like beer style, alcohol content, and user ratings.
- Cleaned the dataset by removing null values and irrelevant columns (beer ID, user profile, etc.).
- Reduced the size of the rating matrix for computational efficiency by selecting the top 4000 users and beers with the most interactions.

### Modeling:
1. **K-Nearest Neighbors (KNN)**:
   - Applied KNN to identify similar users and predict their ratings for beers they haven't yet reviewed.
   - Evaluated model performance using **Mean Square Error (MSE)** and **Root Mean Square Error (RMSE)**.

2. **Singular Value Decomposition (SVD)**:
   - Used SVD for matrix factorization to learn latent features from user-item interactions and predict missing ratings.
   - Optimized hyperparameters with a grid search and compared performance with KNN.

### Clustering:
- Performed clustering using the **K-Means** algorithm to group users with similar preferences.
- Evaluated the quality of clusters with the **Silhouette coefficient**, but results showed significant overlap, likely due to the high sparsity of the rating matrix (94% missing values).

## Results
- Both **KNN** and **SVD** successfully completed the sparse rating matrix. However, **SVD** outperformed KNN in terms of prediction accuracy, with a final RMSE of 0.616.
- The recommender system identified beers with high predicted ratings for users, showing a bias toward popular beers.
- The clustering analysis did not yield meaningful user segments due to data sparsity, but potential improvements could involve using different distance measures or more advanced clustering algorithms.
