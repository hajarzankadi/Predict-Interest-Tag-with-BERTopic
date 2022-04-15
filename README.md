#Using BERTopic and BERTweet transformer to predict interest tag from tweets

In this tutorial, we are going to elaborate a step by step process to detect interest tag from tweets.

The process starts from data cleaning which includes removing URLS, numbers, emojis, punctuation, etc. Then, we will create the BERTopic model.

Before starting, I will highlight some important details:

1. BERTopic:

BERTopic is a topic modeling technique that leverages 🤗 transformers and c-TF-IDF to create dense clusters allowing for easily interpretable topics whilst keeping important words in the topic descriptions as highlighted in here.

The algorithm is based on 3 stages:

    - Extract document embedding with BERT or any other embedding technique
    - Clustering documents which uses: UMAP as a dimentionality reduction of embeddings and HDBSCAN to cluster reduced embeddings and create clusters of semantically similar documents
    - Creating topic representation by : Extracting and reducing topics with c-TF-IDF and improving coherence and diversity of words with Maximal Marginal Relevance

 for more details, I advice you to check out this link.

2. BERTopic installation:

The package is installed via pypi:

    pip install bertopic

3. BERTweet:

BERTweet is the first public large-scale language model pre-trained for English Tweets. BERTweet is trained based on the RoBERTa (A Robustly Optimized BERT Pretraining Approach) pre-training procedure.

for more details, please check out those two references: BERTweet and Roberta.

4. dataset:

For this tutorial, I used this Kaggle dataset, which contains data analysis tweets from verified accounts on Twitter from 2010-2021.

5. Tweet preprocessing:

In order to preprocess our tweets, I use “tweet preprocessor” package, a preprocessing library for tweet data written in Python and that can be installed via :

— using Pip:

    pip install tweet-preprocessor

— using Anaconda:

    conda install -c saidozcan tweet-preprocessor

the script is highlighted in the file named Predict-Interest-Tag-with-BERTopic.ipynb
