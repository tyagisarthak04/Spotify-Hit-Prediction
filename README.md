# Spotify-Hit-Prediction

# Project Scope

The dataset by Farooq Ansari has features for tracks fetched using Spotify's Web API, base on the tracks labeled hit or flop by the author, which can be used to make a classification model to predict whether any given track would be a 'Hit' or not. While the original Kaggle dataset was created by Ansari, I created my own machine learning model to analyze the songs, and then further analyzed the data for a retrospective analysis of features for songs from each decade (1960s - 2010s)..

# Metadata Summary

The original data, retrieved through Spotify's Web API (accesed though the Python library Spotipy), includes 40,000+ songs with release dates ranging from 1960-2019. Each track is identified by the track's name, the artist's name, and a unique resource identifier (uri) for the track.

The dataset includes measurements for the following features, defined and measured by Spotify for each track:

    danceability
    energy
    key
    loudness
    mode
    speechiness
    acousticness
    instrumentalness
    liveness
    valence
    tempo
    duration (in milliseconds)
    time signature
    target (a boolean variable describing if the track ever appeared on Billboard's Weekly Hot-100 list)

Two additional features were defined by Ansari and extracted from the data recieved by the API call for Audio Analysis of each particular track:

    chorus hit (an estimation of when the chorus of the track would first appear, i.e. "hit")
    sections (number of sections inside the song)

# Methodology

The team trained and tested 4 different models to evaluate the dataset, in addition to variations within some of the models.
   
    KNeighborsClassifier
    Logistic Regression
    Random Forest Model
    AdaBoostClassifier
    Artificial Neural Network/Deep Learning Model

# Logistic Regression
  roc train score : 0.8780120318203887
  roc test score : 0.9055711092658175
  
# RandomForestClassifier
 
  roc train score : 0.9999998974409254
  roc test score : 0.9286429323977039
  
# AdaBoostClassifier
  
  roc train score : 0.920649736351387
  roc test score : 0.9126342806691633
  
# KNeighborsClassifier

  roc train score : 0.920649736351387
  roc test score : 0.9126342806691633

# Random Forest as Final Model

  In this case, the best variation of the model was with Standard Scaler normalization. With this model, I was able to see immediately that no one feature seemed   to have a particularly strong weight or influence on the overall results:
  
# Results of final model
  
  p_score 0.8420168067226891
  r_score 0.8994614003590664
  f1 score 0.8697916666666666
  Accuracy Score 0.8677536231884058
  
After running the 4 models and the variations described above, I chose the Random Forest model with adjusted settings as the final model, given that it had produced the best results with the highest levels of accuracy.
    

