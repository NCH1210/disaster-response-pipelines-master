# Disaster-Response-Pipeline Project

In this project a data set provided by Figure Eight has to be analyzed to build a model for an API that classifies disaster messages.
As a result, the machine learning pipeline should categorize emergency messages based on the underlying problem of the sender.

### Instructions
1. The the following commands in the project's root directory need to be carried out in order to set up the database and model.

    - ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/

### File Descriptions

`process_data.py`: A ETL Pipeline that 
- loads the `messages` and `categories datasets`
- merges the two datasets
- cleans the data
- stores it in a SQLite database

`train_classifier.py`: A Machine Learning Pipeline that
- loads data from the SQLite database
- splits the dataset into training and test sets
- builds a text processing and machine learning pipeline
- trains and tunes a model using GridSearchCV
- outputs results on the test set
- exports the final model as a pickle file

`run.py`: A Flask Web App that visualizes the results

### Licensing, Authors, Acknowledgements

Data has been provided by Figure Eight.