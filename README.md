# Recommender System with Collaborative Filtering

An example of applying collaborative filtering on recommender system for dating platform.

Datasets are stored on `datasets` and `toy_datasets`.

Due to the large amount of data on the libimseti dataset, we didn't include in this repository. You may download it [here](https://networkrepository.com/rec-libimseti-dir.php). Toy datasets are provided as references.

# Contributing

## Getting started

1. Edit the `datasets_loc` to change the dataset.
2. You can run cell by cell, or run the entire project but only run **before the visualization part**.
3. To see the visualization, run the one according to your dataset. For example, if you are using the toy dataset, run only the "For small dataset visualization".

## Variables

**`ratings` -** Raw data from `ratings.csv`. A pandas dataframe with columns `"UserID"`, `"ProfileID"`, `"Rating"`. Each row is a rating of a user to a profile.

**`user_ratings` -** Pivot table generated from `ratings`. Each row is a user and each column is a profile. The value is the rating of the user to the profile.

**`user_ratings_df` -** Dataframe generated from `user_ratings`. Removed value label.

**`predicted_ratings` -** Predicted ratings matrix.

**`recommendations` -** Recommendations array with tuple of (`profile_id`, `predicted_rating`)

## Current progress

- [x] Toy example with mapped info, `"Gender"`, `"Name"`
- [x] Implemented profile-based (item-based) CF recommender system, with KNN neighbor algorithm using cosine similarity.
- [x] Fix predicted score on `predict_rating_with_neighbor_correlations`
- [x] Fix: Now assuming if user did not vote -> dislike (Different approach in cosine and jaccard)
- [x] Support recommendation for large dataset
- [x] Try jasscard similarity to predict rating
- [x] Fix training data and test data split is incorrect
- [x] Turn item-based into user-based
- [ ] Confusion matrix
