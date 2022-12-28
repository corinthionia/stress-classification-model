# 2022-2 Stress Types Classification with MultinomialNB and Rogistic Regression

# Data

[Stress Analysis in Social Media](https://www.kaggle.com/datasets/ruchi798/stress-analysis-in-social-media/code) in Kaggle

The data consists of `dreddit-train.csv` and `dreddit-test.csv`. You can use those data by unzipping the `data.zip` or downloading in kaggle.

# Accuracy

- Multinomial Naive Bayes: 0.5699614890885751
- Logistic regression: 0.5298087739032621

# Analysis on the poor result

## The problem of the data

### Data imbalance

- The number of text data differed a lot by category.
- We removed the four categories with the smallest number of data and trained the model again. Nevertheless, no significant results were obtained.

### Incorrectly labeled

- We use subreddit column for classification. However, it is not the result of classifying categories by analyzing the context of the sentence. They are just designated by the user when writing a post.

### The limitations of word-appearance-based vectorization

- As you can see in the word cloud, the words in types are very similar. Therefore, it is difficult to produce accurate results through vectorization based on the number of word appearance.
