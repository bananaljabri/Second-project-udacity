# Second-project-udacity

Disaster Response Web App

You will need these libraries:

json, sklearn, sqlalchemy, sys, numpy, re, pickle, warnings, plotly, pandas, nltk, flask.


Repository Contain:
This repository contains code for a web app which an emergency worker could use during a disaster event, to classify a disaster message into several categories, in order that the message can be directed to the appropriate aid agencies.

The app uses a ML model to categorize any new messages received, and the repository also contains the code used to train the model and to prepare any new datasets for model training purposes.

Project files:

Processing data, building an ETL pipeline to extract data from source, cleaning the data and saving it in a SQLite DB.

Build a machine learning pipeline that can classify tweet text messages into 36 different categories.

Running a web application which can show model results in real time.


How to run?

To run ETL pipeline for cleaning data and store the processed data in the database:

Run the below command from the terminal-

python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db
To run the ML pipeline that loads data from DB, trains classifier and saves the classifier as a pickle file:

Run the below command from the terminal-

python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl
Run the following command in the app's directory to run your web app-

python run.py
Open a browser and go to http://0.0.0.0:3001/. 
