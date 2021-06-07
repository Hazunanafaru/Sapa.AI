# Sapa.AI

![sapaai-removebg-preview](https://github.com/Hazunanafaru/Sapa.AI/blob/main/images/sapaai.png)

Git repository for Sapa.AI (Bangkit Capstone Project by Neutr.AI (B21-CAP0093) Team.

# Description
The PPPA Ministry noted that in 2020 there were 4,116 cases of violence against women and children in Jakarta (a period of 7 months). Our independently conducted survey shows that almost 97 percent of the respondent doesn’t report the violence they have experienced or seen. However, the reporting system is still manual and not optimized. With SAPA AI there will be more and more ways available for victims to report cases of violence and make the process of handling reports more effective and efficient for the ministry of PPPA (Perlindungan Perempuan dan Anak) with the availability of additional features from SAPA AI. With the Deep Learning algorithm, we can create a reporting platform that directly classifies the types of violence experienced with the appropriate services. Through this initiative, we want to contribute to emancipated women and protect the future of our children.

# Usage

# Contributors
## Android | Akbar Adi Susanto (A1941930) and Rizkina Maulida Safira (A2142082)
The application of Firebase in the application for  login (authentification), account registration, and form (real-time), the application is connected to APIs from the cloud to then connect data from Android and stored in the database. The application can also save audio files to the Android internal storage, which can then be forwarded and managed by machine learning until it gets the desired classification.

You can see our Android development progress in [android-development branch](https://github.com/Hazunanafaru/Sapa.AI/tree/android-development)

## Machine Learning | Muhammad Fauzan (M0080906) and Mutiara Annisa (M1941928)
we created the Indonesian reporting text dataset from the internet and we made our own survey to get an additional dataset for our machine learning model. After we preprocessing our data, then we apply to train a model to classify the reports into the Ministry of PPPA service classes. We split the dataset into train set and dev set to evaluate the model performance. We also tuned the hyperparameters to find the best-performing model. We made a function to get the desired results. Finally, we exported the best model in .pb format to be deployed in the Google Cloud Platform.

You can download our dataset in this link : https://www.kaggle.com/fafafwzn/indonesia-violence-reporting-text

## Cloud Computing | Husni Naufal Zuhdi (C0080903) and Sanding Riyanto (C1941940)
![Diagram Cloud Computing](https://github.com/Hazunanafaru/Sapa.AI/blob/main/images/mvp_diagram.jpeg)

Build a REST API for our android app with Google Cloud Run and build a Machine Learning Model with AI-Platform. We also use Speech-To-Text API to process the recorded voices into a text so our Machine Learning Model can ingest the voice-recorded reports.

This is our example for Speech to Text and Machine Learning model results

![STT](https://github.com/Hazunanafaru/Sapa.AI/blob/main/images/result_text.png)

![ML](https://github.com/Hazunanafaru/Sapa.AI/blob/main/images/result_services.jpeg)

# Credits
![Bangkit](https://github.com/Hazunanafaru/Sapa.AI/blob/main/images/bangkit.png)

This project are part of capstone project for Bangkit 2021

# Changelog
10/05/21/a : Make ml-development branch

10/05/21/b : Update README.md

12/05/21/a : Creating a machine learning model using self-made violation-complaint-dataset to classify texts into complaint classes. Adding an ipynb file containing experiments of many different NLP approach to solve the problem. Decided to use the lowermost approach, which is using pretrained language model in bahasa Indonesia, followed by layers of neural network to do classification task. This approach resulting a low loss value and having high F1 score. Also, when we do an inference to the model, it gives us an intuitive result. Finally, the model is exported in .h5 format.

14/05/21/a : First version of our classification model to classify reporting texts into 8 classes. Loss is pretty low, the prediction result is also intuitive enough

18/05/21/a : This commit add an .ipynb file containing our process in developing speech recognition (speech-to-text) machine learning system, which is then considered the development to be dropped as the regulation permit us to use google automatic speech-to-text as long as we create another original model.

24/05/21/a : Update folders and add machine learning model

29/05/21/b : Update front-panick and machine learning services

29/05/21/c : Tidy up some folders

30/05/21/a : Make Speech-to-text and machine learning python files

30/05/21/b : Move service account key json files to cloud storage

31/05/21/a : Start build REST API with Flask

03/06/21/a : First Trial to Deploy the CLoud Run with Mock Database (SQLALCHEMY)

06/06/21/a : Finish API

06/06/21/b : Fix Speech to text result

06/06/21/c : Clean up the README files

06/06/21/d : Clean up files
