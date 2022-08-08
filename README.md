# New Yor Times Tech articles | NLP Analysis | KNN Clustering 📄📚📊

The main objective of this project is to differentiate topics in a set of articles on technology published in the new york times. To achieve this we will use text mining and clustering.

## Technologies
* Python
* Jupyter

### Python Libraries 🗃️

* Numpy
* Pandas
* Matpltlib
* Scikit-learn
* Keras
* re
* Nltk
* WorkCloud
* Tfidf
* PCA

## Data 📁

The dataset contains 1,200 technology articles published in the New York Times. It has two columns: 

  * Title of the article
  * Abstract of the article
  
## Text mining ⛏️

* First of all, we eliminate the "stopwords" from the abstract column, discarding irrelevant words to reduce the dimension later, facilitating the training of the model.
* We convert each word of the abstract to tokens in order to work with them.
* We eliminate the words that only appear once and the numbers, since when creating clusters they do not give us anything.
* We convert each word to its stem to be able to group them later in clusters.
* We get the Tf-idf array and convert it to a dataframe to work with.

## Clustering 🟡🔴🟢

Now that we have done the preprocessing of the text we can start working with the dataset that we have created and use clustering techniques to try to identify topics and group the articles.

The first thing we do is use PCA to reduce the dimensionality of our dataset. In this case we chose 500 components with explained variance of 80%.

![image](https://user-images.githubusercontent.com/105368099/183402363-9966a9b8-fad1-4682-8e8a-0a71d691638d.png)

Afterwards, we used different techniques to try to obtain the optimal number of clusters and we carried out different tests and post-analysis of the results obtained with metrics and visualization tools.

![image](https://user-images.githubusercontent.com/105368099/183402780-4b620a12-7e7d-4791-b782-8195ad929937.png)

## Conlusions

* All the news are on very similar topics, therefore difficulties arise when performing clustering. Even so, our models are capable of isolating topics that are out of the most common news.

* Using a PCA of 500 components and testing kmeans with different numbers of centroids, the result always gives us a cluster with 50/60% of the articles grouping news on less specific topics. The rest of the groups do have more marked themes, social networks, amazon, theranos, silicon valley...

* On the one hand, the clusters are very close to each other, but it is true that all the news is about the same thing. On the other hand, it has been able to differentiate some topics such as social networks.


