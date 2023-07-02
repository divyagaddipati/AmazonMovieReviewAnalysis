# Amazon Movie Recommendations

<!-- TABLE OF CONTENTS -->
## Table of Contents

* [About the Project](#about-the-project)
  * [Dataset](#dataset)
  * [Technologies](#technologies)
  * [Installation](#installation)
* [Contact](#contact)
* [Note](#Notes)
* [Sources](#acknowledgements)



<!-- ABOUT THE PROJECT -->
## About The Project
* Develop a model to work toward improving movie recommendations that can be used in recommending movies to a user in order to increase engagement. 
* Perform sentiment analysis on the reviews to gain deeper understanding on how users rate movies/tv shows.
* Perform topic modeling to gain insights on the kind of content/genre that is popular or various factors users look at while providing reviews. 

<!-- DATASET -->
## Data Set
Dataset used for the project can be found in the below link:

<a href="http://jmcauley.ucsd.edu/data/amazon/index_2014.html">Amazon Movie and TV Reviews Dataset</a>

<br />
The dataset we used is the Amazon Product data: reviews_Movies_and_TV_5 from UCSD's Machine Learning Repository. The dataset contains 1,697,533 reviews of movies and tv shows. The features include:

* reviewerID - ID of the reviewer, e.g. A2SUAM1J3GNN3B
* asin - ID of the product, e.g. 0000013714
* reviewerName - name of the reviewer
* helpful - helpfulness rating of the review, e.g. 2/3
* reviewText - text of the review
* overall - rating of the product
* summary - summary of the review
* unixReviewTime - time of the review (unix time)
* reviewTime - time of the review (raw)

We are primarily concerned with the reviewerID, asin, and overall (Rating) for content recommendations. We will also explore the review text and summary with sentiment analysis and topic modeling. Network analysis of the bipartite graph generated from reviewers to products will also be conducted.

<br />

<!-- TECHNOLOGIES -->
## Technologies
* Sklearn (Surprise)
* Pandas, Numpy 
* VADER
* NLTK
* SpaCy 
* Supervised Machine Learning techniques

<!-- INSTALLATION -->
### Installation
```
cd AmazonMovieRecommendations
pip install -r requirements.txt
jupyter notebook
```

<!-- NOTES -->
### Notes

* ContentRecommendations.ipynb takes a significant amount of time for hyper parameter selection and training models / k-fold cross validation.

* Only reviewers with atleast 100 reviews were included in the dataset to 1. reduce run time and 2. have only the reviewers with a significant amount of reviews.

* Network Analysis code takes significant amount of time to find metrics

* NetworkAnalysis_src_target_reviews_Movies_and_TV_5.csv is the data used to generate bipartite graph, and reviews_Movies_and_TV_5.json.gz is the data used for all other parts of assignment. 



<!-- CONTACT -->
## Contact
Conrad Pereira          conradpereira@vt.edu

Divya Gaddipati         divyaj@vt.edu

<!-- SOURCES -->

### Sources

[1]  http://jmcauley.ucsd.edu/data/amazon/index_2014.html

[2] https://surprise.readthedocs.io/en/stable/getting_started.html
