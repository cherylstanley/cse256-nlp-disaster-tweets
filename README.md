# NLP Disaster Tweets



## How do you determine whether a tweet refers to a disaster to not?
* In the age of social media, as smartphones have become an increasingly ubiquitous form of communication, Twitter has become a more and more widespread and commonly used tool for signalling immediate communication. This includes bringing attention to disasters and news coverage for current events in a non-traditional way. But sometimes content flagging mechanisms in Twitter may have trouble categorizing tweets as to whether or not they refer to a disaster due to missing context that AI might not have. Can we really train AI to categorize tweets correctly given that they have to learn this context for themselves?

* This project seeks to answer that very question, by utilizing sentiment analysis and natural language processing to categorize tweets from a dataset, assigning a binary label target value of 0 or 1, to predict whether or not the tweet is referring to a disaster. 

* The dataset was obtained from Kaggle and contains thousands of tweets labelled as positive or negative as it relates to whether or not they relate to disasters. The dataset can be found at this link : https://www.kaggle.com/competitions/nlp-getting-started/overview

Now the naive solution would be to simply flag certain words (`hurricane`, `blaze`, `downpour`, etc.) as being likely to refer to a disaster but this may have unintended consequences as it doesn't take into account linguistic patterns and slang which could see them being used in a positive connotation. See the example below for reference to this phenomenon of seemingly disaster-related words being used in a positive context.

![image](https://github.com/user-attachments/assets/acd3d91b-de4f-4394-8878-09824d64bdaf) 


### In the above image, the author explicitly uses the word `ABLAZE` but means it metaphorically. This is immediately clear to you or I or any other human, especially with the visual aid. But it's less clear to a machine without the context to human language and linguistic expressions that we have.

My approach saw a baseline accuracy of **73.64%** using neural networks, with an improvement of up to **83.64%** accuracy through an implementation of an advanced DistiliBERT model.

I experimented with multiple hyperparameters including batch size, number of epochs, and pretrained embeddings to achieve a greater accuracy for this model and learned a lot through error analysis and employing techniques learned from different research papers experimenting with similar datasets and goals.

My findings from this research were summarized and contained in a final research report which can be found in the main directory of this repository! Thank you for reading
