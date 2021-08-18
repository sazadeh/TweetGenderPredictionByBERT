# TweetGenderPredictionByBERT

There are some pre-trained BERT models introduced by Hugging Face (https://huggingface.co/transformers/pretrained\_models.html).\\
We used the transformer library created by @ThilinaRajapakse (https://github.com/thilinarajapakse/simpletransformers) 
used those pre-trained models by Hugging Face in it. Then try to predict the gender of tweets based on the tweet text.

We wanted to predict the gender-based on their tweet. We found a data set (https://www.kaggle.com/crowdflower/twitter-user-gender-classification)
that has a gender for each tweet. We did the pre-processing steps on tweet text and considered the genders, female or male (we ignored unknown genders).
Also kept the genders have the *gender-confidence > 0.80*. Then we used **CountVectorize** library to convert the text into vectors.
We changed *female* to *0* and *male* to *1* . The *gender* column is considered as our label.
Then we trained the BERT model based on different models such as **Bert, DistilBERT, RobertA** by this Simple Transformer library. 

We choose the **distilbert classification model** then *predict* the genders based on our primary data set. 
We got the main Data set from (https://www.kaggle.com/gpreda/covid19-tweets) and then pre-processed tweet texts such as removing emojis,
stop words, URLs, Username and Stemming. Furthermore, we used *VaderSentiment Package* to generate the Sentiment of tweets and then saved the clean tweet text
and sentiments as "clean_tweets_sentiment.csv" file. We used this file as a primary clean dataset to predict the gender based on the trained model.

The best accuracy we could get from these models was 61%. For future studies, it is better to annotate gender for a tweet dataset based on text, username, and 
description and then use this annotated data set for tarin the models. It might help to get better accuracy.

