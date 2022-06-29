# Second-project-udacity

Disaster Response Web App

You will need these libraries:

json, sklearn, sqlalchemy, sys, numpy, re, pickle, warnings, plotly, pandas, nltk, flask.


Repository Contain:
This repository contains code for a web app which an emergency worker could use during a disaster event, to classify a disaster message into several categories, in order that the message can be directed to the appropriate aid agencies.

The app uses a ML model to categorize any new messages received, and the repository also contains the code used to train the model and to prepare any new datasets for model training purposes.

Project files:

1- process_data.py: This code takes as its input csv files containing message data and message categories (labels), and creates an SQLite database containing a merged and cleaned version of this data.

2- train_classifier.py: This code takes the SQLite database produced by process_data.py as an input and uses the data contained within it to train and tune a ML model for categorizing messages. The output is a pickle file containing the fitted model. Test evaluation metrics are also printed as part of the training process.

3- ETL Pipeline Preparation.ipynb: The code and analysis contained in this Jupyter notebook was used in the development of process_data.py. process_data.py effectively automates this notebook.

4- ML Pipeline Preparation.ipynb: The code and analysis contained in this Jupyter notebook was used in the development of train_classifier.py. In particular, it contains the analysis used to tune the ML model and determine which algorithm to use. train_classifier.py effectively automates the model fitting process contained in this notebook.

5- data: This folder contains sample messages and categories datasets in csv format.

6- app: This folder contains all of the files necessary to run and render the web app.

How to run?

1- Run process_data.py

Save the data folder in the current working directory and process_data.py in the data folder.

From the current working directory, run the following command: python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db

2- Run train_classifier.py

In the current working directory, create a folder called 'models' and save train_classifier.py in this.

From the current working directory, run the following command: python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl

3- Run the web app

Save the app folder in the current working directory.

Run the following command in the app directory: python run.py

Go to http://0.0.0.0:3001/
