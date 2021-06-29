# Classifying type of sexual harassment with personal stories
![scource ](https://github.com/bhaveshnaidu999/sexual-harassment-classification-project/blob/main/images/meto.jpg)
## Overview:
As with the rise of #MeToo, an increasing number of personal stories and experiences about sexual harassment and sexual abuse have been shared online. This vast amount of online data could be put to some meaningful work. As there has not been much research and analysis done on this kind of dataset this provides us with great opportunities to work on problems related to the social cause. This case study tries to automatically categorize various forms of sexual harassment, based on stories shared on the online forum SafeCity for the labels of groping/touching, ogling/staring, and commenting  This automatic classification of different forms of sexual harassment can help victims and authorities to partially automate and speed up the process of filling online sexual violence reporting forms. Inspiration for this project was taken form this ![research paper](https://arxiv.org/pdf/1809.04739.pdf)

## Problem Statement:
Predict the types of sexual harassment given a description on the incident the incident may belong to one , more or none of the three categories of sexual harassment namely commenting, goping/touching and ogling/staring

For Example : The description "My college was nearby. This happened all the time. Guys passing comments, staring, trying to touch. Frustrating" is positive for three classes: commenting, ogling/staring, and touching/groping.

## Scource of the Data:
Data Source : https://github.com/swkarlekar/safecity

The Data set consist of one folder multi-label classification(multilabel_classification)
multilabel_classification folder consist of three cvs files for train, dev and test set.
The Data for multi-label classification consists of four columns with first column being the description 
of the incident and and the second, third, and fourth column being 1 if the category of sexual harassment
is present and 0 if it is not.

![scource ](https://github.com/bhaveshnaidu999/sexual-harassment-classification-project/blob/main/images/multi-label%20folder.png)

There are 7201 training samples, 990 development samples, and 1701 test samples.

Top 5 records form train data
![scource ](https://github.com/bhaveshnaidu999/sexual-harassment-classification-project/blob/main/images/head.png)

## Machine Learning problem:
Multi-label Classification : Building a Multi-label Classification for predicting multiple categories simultaneously for the same input

## Evaluation metrices for multi-label classification:
As it is a multi-label classification problem the evaluation metrices used was hammimg loss and other few metrices where also monitored.
Hamming loss is defined as 

![scource ](https://github.com/bhaveshnaidu999/sexual-harassment-classification-project/blob/main/images/hamming%20loss.png)

Here I experimented with different machine learning  with different featurizations like tf-idf, tf-idf weighted word2vec GloVe Embedding of words, FastText Embedding and different deeplearning algorithms like bidirectional lstm, cnn, etc. 

## All Machine Learning Models with different featurization:
![scorce](https://github.com/bhaveshnaidu999/sexual-harassment-classification-project/blob/main/images/ML%20model.png)
Logistic Regression with FaxtText embedding of words and characters gives the lowest hamming loss.

## All Deep Learning Models with different featurization:
![scorce](https://github.com/bhaveshnaidu999/sexual-harassment-classification-project/blob/main/images/DL%20models.png)
Bi-LSTM + CNN Conv1D model with FastText embedding of words and character gives lowest hamming loss of 0.1593 which is an imporvement over the best model for multi-label classification mentioned in the ![research paper](https://arxiv.org/pdf/1809.04739.pdft)

# Final Pipeline
final pipeline with the best model which is Bi-LSTM+ CNN Conv1D looks like this
![](https://github.com/bhaveshnaidu999/sexual-harassment-classification-project/blob/main/images/pipeline.png)

# Deployment:
Building a web app with ![streamlit](https://streamlit.io/) and deploying it on ![heroku](https://dashboard.heroku.com/login)

![](https://github.com/bhaveshnaidu999/sexual-harassment-classification-project/blob/main/images/deploy.gif)

link to web app : comming soon

if you want to learn more about the project the please read the detailed blog i have written on medium 

link to the blog : https://medium.com/@bhaveshnaidu999/classifying-type-of-sexual-harassment-with-personal-stories-2994ca7b3ee1

### connect with me on
[![LinkedIN Connect](https://img.shields.io/badge/Linkedin-connect-blue)](https://www.linkedin.com/in/bhavesh-naidu-23bb52199?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3B4EZqZ2Q%2FQd2QiO%2BZEhU68A%3D%3D)
[![MAIL](https://img.shields.io/badge/-bhaveshnaidu999@gmail.com-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:bhaveshnaidu999@gmail.com)](mailto:bhaveshnaidu999@gmail.com)

If you happen to have any query or Feedback please connect with me.

