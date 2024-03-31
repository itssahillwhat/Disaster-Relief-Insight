# Project Overview
* In this project, we delve into the analysis of numerous authentic messages transmitted during natural disasters, sourced from various channels including social media platforms and direct communication with disaster response organizations.

* An Extract, Transform, Load (ETL) pipeline is constructed to handle the preprocessing of message and category data extracted from CSV files, facilitating their integration into a SQLite database.

* Additionally, a machine learning pipeline is devised to categorize these messages, directing them to the appropriate disaster relief agencies based on their content and context.

* Furthermore, the project encompasses the development of a user-friendly web application, equipped with insightful visualizations. This application aids emergency personnel in efficiently classifying new messages across a spectrum of 36 categories.

* The deployment of machine learning techniques is pivotal in assisting diverse organizations in discerning the relevance of incoming messages and prioritizing them accordingly.

<hr/>

## Components
The project comprises three key components:

1. ETL Pipeline (process_data.py): This component orchestrates a meticulous data cleaning process, which involves:

   * Loading datasets containing messages and their respective categories.
   * Integrating and merging these datasets.
   * Executing data cleansing operations.
   * Storing the refined data into a SQLite database.


2. ML Pipeline (train_classifier.py): This pipeline is dedicated to the implementation of machine learning methodologies, encompassing:
   * Retrieving data from the SQLite database.
   * Partitioning the dataset into training and testing subsets.
   * Constructing a comprehensive text processing and machine learning pipeline.
   * Training and fine-tuning a model using GridSearchCV.
   * Evaluating model performance on the test set.
   * Exporting the finalized model as a pickle file.


3. Flask Web App: This component represents the user interface, designed using Flask framework, featuring:
   * Integration of Plotly for data visualization within the web application.
   * Facilitation of message classification by emergency responders.

<hr/>


## Commands for setting up your database and model:


* To initialize the database and model setup, execute the following commands from the project's root directory:

* For the ETL pipeline, which cleans the data and stores it in the database:


    python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db


* For the ML pipeline, responsible for training the classifier and saving the model:


    python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl


* To launch the web application, navigate to the app's directory and run the following command:
    

    python run.py


* These commands ensure the seamless setup and execution of the project components.




