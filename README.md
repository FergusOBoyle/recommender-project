# recommender-project

Article recommender for users of IBM Watson Studio

In this python notebook, I compare a couple of methods of collaborative filtering: neighbourhood (a.k.a memory-based) and matrix factorization (a.k.a model-based) by way of Singular Value Decomposition (SVD).

The data used describes IBM Watson Studio user access to articles on the website. The goal of the recommender is to recommend articles likely to be of interest to the users.

The feedback is implicit in that all we hav to go on as a measure of user preference is a record of user-item interaction. 

## Summary of results

The dataset of individual user-item interactions was split into a training set and a test set. Both sets contain a fair degree of overlap in terms of users as many users in the dataset have accesses more than 1 article.

Each algorithm is trained on the training data subset (with the exception of the random recommender which does not need training). Recommendations made for each of the users in the test dataset are then compared to the actual test data subset.

TODO: F1_score details

| Reecommender  | F1 Score |
| ------------- | ------------- |
| Random     | 0.017  |
| Rank-based  | 0.058 |
| SVD Collaborative | 0.198 |
| Neighborhood | 0.187

## Discussion

Clearly even the best performing of the algorithms does not perform so well. Implicit preference feedback is inevitably less reliable due to such things as clicks on a article due to click-baiting etc.  


## Packages

The analysis is delivered in the form of a Jupyter Notebook. This can be installed using Anaconda (see below).

Required packages are specified in requirements.yml.

## Installation



## Data

The 2 data files used for this project were obtained from Udacity.com as part of their Data Science Nanodegree program. Files are contained in the data/ subfolder.
