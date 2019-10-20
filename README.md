# Data Scientist Nanodegree Capstone 
Capstone project for the Udacity Data Scientist Nanodegree. The goal of this project is to use Apache Spark to investigate and model music streaming data to predict when a user is going to cancel their account. Udacity provided four different prompts for the final project. I chose this project because it was the only one that required the use of Spark. I wanted to enhance and demonstrate my skills in Spark. 

We were provided with a very small subset of the data to which I used to set up my code in a jupyter notebook locally. We then could run analysis on a very large data set ( ~25 million rows ) using an AWS EMR cluster or use a medium sized dataset (~500 thousand rows ) using IBM Watson Studio. I originally performed this analysis connected to an AWS EMR cluster but finished the project using IBM Watson Studio. I go into these issues more later in the report. 

## Check these out 
#### Blog Post on Medium 

#### HTML Version of Notebook

## Data
The data was provided by Udacity and is intended to simulate music streaming logs from a company such as Spotify or Pandora. 

## Overview
* Process data
* Visualize some intuitions
* Create features
* Implement classification algorithms
* Tune models
* Evaluate trained models


### Processing
* Remove null values for timestamp columns 
* Add column 'churn' which represents if the event was an account cancellation event
* Convert timestamps to a readable format and compute difference between the time of the event and the time the user registered and store it in the variable 'days_since_reg'

### Visualizng
I visualized some intutions I had about the data. My intuitions that were most clearly supported by the visuals are

How long a user has had their account

The variety of artists listened to 

Average number of songs in a session 

### Creating Features 

From the log data I created a dataframe with one row for each user and the following features

* Status ( Paid or Free )
* Days since registration
* Number of "Thumbs Up" given
* Variety of artists listened to
* Average length of listening session
* Number of songs added to a playlist


### Classification Algorithms 
I implemented and tuned the following models with the following results 

