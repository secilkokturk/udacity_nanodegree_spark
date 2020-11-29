# udacity_nanodegree_spark
udacity_nanodegree_spark project

# Definition
This project is the final project of Udacity Nanodegree Data Scientist.
I have completed the Sparkify project which is Churn Prediction on a music app event database using Spark.

# Libraries
The libraries used are:
pyspark
pandas
numpy
datetime
matplotlib
itertools
sklearn

# Data
The data is an event log data coming from two months of history from a music playing app. The data includes many events such as login, logout, song play, next song, thumbs up, upgrade, cancel, etc.

The columns are:
artist: Song Artist's Name
auth: Authorization Level (Logged Out, Logged In, Cancelled, Guest)
firstName: Name of User
gender: Gender of User (F, M, Null, provided M or F if the user is registered/logged in or out)
itemInSession: Item Number
lastName: Lastname of User
length: Session Length
level: Subscription Type (paid, free)
location: Town and state name
method: (PUT, GET)
page: Sort of like the event type (NextSong, Home, Error, etc.)
registration: Registration Id
sessionId: Session Id
song: Song Name
status: Http Status (200, 307, 404)
ts: timestamp (epoch)
userAgent: Browser Info
userId: User Id

# Features

Features are computed using the various type of information in the event log data.
Features calculated from pages information:
total_interactions: number of total interactions per user
- homepage_lands: number of home page lands by user Id
- nextsongs: number of nextsong by user Id
- thumbsup: number of thumbsup by user Id
- thumbsdown: number of thumbsdown by user Id
- thumbs_upanddown: number of like and dislike interactions by user Id
- add_to_playlist: number of add to playlist by user Id
- add_friends: number of add friends by user Id
- roll_advertisement: number of roll advertisement by user Id
- setting_pages: number of setting pages by user Id
- help_pages: number of help pages by user Id
- upgrade_pages: number of upgrade pages by user Id
- about_pages: number of about pages by user Id
- save_settings: number of save settings pages by user Id
- error_pages: number of error pages by user Id
- submit_upgrades: number of submit upgrade pages by user Id
- submit_downgrades: number of submit downgrade pages by user Id
- logouts: number of logouts by user Id

Features Calculated from other columns:
-artist_count: how many different singers did the user listened to
- song_count: how many different songs did the user listened to
- session_count: number of sessions
- tenure: tenure in the app (max ts minus min ts)
- female, male: encode gender
- http 307 statuses received
- http 400 statuses received
- state name: location state abbreviation
- device type from browser/app info
- put and get methods

Churn is defined by the Cancellation Confirmation event.

A PCA is performed before modeling

# Model
A Random Forest and Logistic Regression model is fitted on the data.
20% of the data is randomly selected for test and % 20 is separated for validation from within the training set.


# Evaluation
F1 score is used in order to improve the model
The Logistic Regression Model presented a higher accuracy (84%) and a higher F1 (36%) with respect to the random forest which had accuracy of (75%) and F1 of (15%).
The logistic regression model presented an F1 Score of 78.6% on the validation data.

# Files 
The bucket includes the .ipynb file, .html file, which have the code along with this README.md file

# Blog Post
I have a detailed blog post about the project on my medium page: https://medium.com/@kokturksecil
Link: https://kokturksecil.medium.com/spark-project-sparkify-bb96feba4d84
