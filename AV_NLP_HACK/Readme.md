## A Comparison of different approaches for Analytics Vidya Hackathon

### Problem Statement

Data consists of an archive of scientific articles. It consists of the abstracts of the article along with some indicators of source of the articles - Computer Science, Mathematics, Physics and Statistics.

The problem requires a tagging of each article to 25 tags.

Tags: Analysis of PDEs, Applications, Artificial Intelligence,Astrophysics of Galaxies, Computation and Language, Computer Vision and Pattern Recognition, Cosmology and Nongalactic Astrophysics, Data Structures and Algorithms, Differential Geometry, Earth and Planetary Astrophysics, Fluid Dynamics,Information Theory, Instrumentation and Methods for Astrophysics, Machine Learning, Materials Science, Methodology, Number Theory, Optimization and Control, Representation Theory, Robotics, Social and Information Networks, Statistics Theory, Strongly Correlated Electrons, Superconductivity, Systems and Control

Each article can have more than 1 tag.

Training data consists of 14004 records and test data for checking in Leaderboard contains XX records.
The evaluation metric is micro F1 score.

### Approaches

A summary of different approaches tried for this problem is presented below along with the Micro F1 score on the validation set.

Basic preprocessing of making words lower case and removing punctuations has been done. Further preprocessing can yield better results.

Note: Topic Columns indicates the indicator columns for Computer Science, Mathematics, Physics and Statistics

| Approach      | Validation F1-Score |
| ----------- | ----------- |
| Count Vectorizer + OneVsRestClassifier + Logistic Regression     | 0.62       |
| TFIDF Vectorizer + OneVsRestClassifier + Logistic Regression   | 0.68        |
| TFIDF Vectorizer With Topic Columns  + OneVsRestClassifier + Logistic Regression   | 0.76        |
| NBSVM with TFIDF Features   | 0.67        |
| NBSVM with TFIDF Features with Topic Columns   |         |
