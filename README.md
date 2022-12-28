# 2022-2 Stress Types Classification with MultinomialNB and Rogistic Regression

# Data

[Stress Analysis in Social Media](https://www.kaggle.com/datasets/ruchi798/stress-analysis-in-social-media/code) in Kaggle

The data consists of `dreddit-train.csv` and `dreddit-test.csv`. You can use those data by unzipping the `data.zip` or downloading in kaggle.

# Accuracy

- Multinomial Naive Bayes: 0.5699614890885751
- Logistic regression: 0.5298087739032621

# Find out the most correlated unigrams & bigrams

[ almosthomeless ]

- Most Correlated Unigrams are: penny, parttime
- Most Correlated Bigrams are: going college, soon possible

[ anxiety ]

- Most Correlated Unigrams are: anxious, anxiety
- Most Correlated Bigrams are: make anxious, panic attack

[ assistance ]

- Most Correlated Unigrams are: gofundme, url
- Most Correlated Bigrams are: gofundme url, amazon wishlist

[ domesticviolence ]

- Most Correlated Unigrams are: domestic, police
- Most Correlated Bigrams are: called police, domestic violence

[ food_pantry ]

- Most Correlated Unigrams are: supermarket, rice
- Most Correlated Bigrams are: new job, food bank

[ homeless ]

- Most Correlated Unigrams are: shelter, homeless
- Most Correlated Bigrams are: ive homeless, homeless shelter

[ survivorsofabuse ]

- Most Correlated Unigrams are: sexual, abuse
- Most Correlated Bigrams are: know think, sexual abuse

# Analysis on the poor result

## The problem of the data

### Data imbalance

- The number of text data differed a lot by category.
- We removed the four categories with the smallest number of data and trained the model again. Nevertheless, no significant results were obtained.
  ![](https://velog.velcdn.com/images/corinthionia/post/e51f3e08-55da-421b-9be3-24b8238b1bd2/image.png){: width="500" height="500"}

### Incorrectly labeled

- We use subreddit column for classification. However, it is not the result of classifying categories by analyzing the context of the sentence. They are just designated by the user when writing a post.

### The limitations of word-appearance-based vectorization

- As you can see in the word cloud, the words in types are very similar. Therefore, it is difficult to produce accurate results through vectorization based on the number of word appearance.
  ![](https://velog.velcdn.com/images/corinthionia/post/4951aef6-65d3-47dd-803f-8e92a2fd2de8/image.png){: width="500" height="500"}
