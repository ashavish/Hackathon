## A Comparison of different approaches for Analytics Vidya Hackathon

### Problem Statement

The data consists of an archive of scientific articles. It consists of abstracts of articles along with some indicators of source of the articles - Computer Science, Mathematics, Physics and Statistics.

The problem requires a tagging of each article to one or more tags out of 25 tags.

Tags: Analysis of PDEs, Applications, Artificial Intelligence,Astrophysics of Galaxies, Computation and Language, Computer Vision and Pattern Recognition, Cosmology and Nongalactic Astrophysics, Data Structures and Algorithms, Differential Geometry, Earth and Planetary Astrophysics, Fluid Dynamics,Information Theory, Instrumentation and Methods for Astrophysics, Machine Learning, Materials Science, Methodology, Number Theory, Optimization and Control, Representation Theory, Robotics, Social and Information Networks, Statistics Theory, Strongly Correlated Electrons, Superconductivity, Systems and Control

Training data consists of 14004 records and test data for checking in Leaderboard contains XX records.
The evaluation metric is micro F1 score.

[Link to problem](https://datahack.analyticsvidhya.com/contest/hacklive-3-guided-hackathon-text-classification/#ProblemStatement)

### Approaches

A summary of different approaches tried for this problem is presented below along with the Micro F1 score on the validation set.

Basic preprocessing of making words lower case and removing punctuations has been done. Further preprocessing can yield better results. Finetuning parameters of the final chosen model can also give a boost.

Note: Topic Columns indicates the indicator columns for Computer Science, Mathematics, Physics and Statistics

| Approach      | Validation Micro F1-Score |
| ----------- | ----------- |
| Count Vectorizer + OneVsRestClassifier + Logistic Regression     | 0.62       |
| TFIDF Vectorizer + OneVsRestClassifier + Logistic Regression   | 0.68        |
| TFIDF Vectorizer With Topic Columns  + OneVsRestClassifier + Logistic Regression   | 0.76        |
| NBSVM with TFIDF Features   | 0.67        |
| NBSVM with TFIDF Features with Topic Columns   |   0.75      |
| Averaged Glove Word Embeddings(100d) + OneVsRestClassifier + Logistic Regression  |   0.55      |
| Universal Sentence Embedding using Keras  |   0.64     |
| Universal Sentence Embedding using Keras with Topic Columns  |   0.72     |
| Fast Text Classifier  |   0.65     |
| BERT Finetuned No Freeze |  0.71      |
| BERT Finetuned No Freeze with Topic Columns |  0.715      |
| Sentence Transformers (bert-base-nli-mean-tokens) |   0.62    |
| Sentence Transformers with Topic Columns (bert-base-nli-mean-tokens) | 0.70       |
