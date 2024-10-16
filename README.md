Project Description
The ETEDSML Project (Exploratory Data Analysis & Student Machine Learning) focuses on building machine learning models to analyze student performance. The project includes end-to-end data processing pipelines for feature extraction, model training, and evaluation. The model training leverages the CatBoost algorithm due to its powerful handling of categorical data and high interpretability.

Features
Data Ingestion: Load data from CSV files and preprocess them for training.
Data Transformation: Clean and transform the data for machine learning models.
Model Training: Use CatBoost for training and evaluation.
Web Interface: Basic HTML templates for interaction.
Logging: Logs all operations for easier debugging.

src
│   ├── components
│   │   ├── data_ingestion.py        # Handles data loading and splitting
│   │   ├── data_transformation.py   # Manages feature engineering and transformation
│   │   └── model_trainer.py         # Trains the model using CatBoost
│   ├── pipeline
│   │   ├── predict_pipeline.py      # Pipeline for model inference
│   │   └── train_pipeline.py        # Pipeline for model training
│   └── templates                    # HTML templates for the web interface
├── artifacts                        # Stores model and preprocessed data
│   ├── model.pkl                    # Trained model
│   ├── preprocessor.pkl             # Preprocessing pipeline
│   └── data.csv                     # Dataset
├── logs                             # Logs of the application and training
├── notebook                         # Jupyter notebooks for EDA and training
│   ├── 1. EDA STUDENT PERFORMANCE.ipynb
│   └── 2. MODEL TRAINING.ipynb
├── app.py                           # Entry point for running the web app
├── requirements.txt                 # Dependencies
├── setup.py                         # Project setup configuration
├── LICENSE                          # License for the project

Installation
To set up the project on your local machine:

Clone the repository:

Run
git clone https://github.com/saffronhamid/ETEDSML-Project.git
cd ETEDSML-Project
Create a virtual environment and activate it:

Run
python3 -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
Install the dependencies:

Run
pip install -r requirements.txt
Usage
To run the web application, execute:

Run
python app.py
Visit the provided localhost link in the terminal to interact with the web interface.

Data Ingestion
Data is ingested from stud.csv located in the data folder. The data_ingestion.py module handles loading and splitting the data into train and test sets.

Data Transformation
The data_transformation.py module applies feature engineering and necessary transformations to the dataset.

Model Training
To train the model using the CatBoost algorithm, the following steps are executed in the training pipeline:

Run
python src.pipeline.train_pipeline.py
Model Training
The model is trained using CatBoost, a gradient boosting algorithm that handles categorical features efficiently.
Output models are saved in the artifacts/ directory as model.pkl and preprocessor.pkl.
Logging
Logs are stored in the logs/ directory. Each session generates a log file with timestamps for better traceability.

Artifacts
model.pkl: The trained CatBoost model.
preprocessor.pkl: The preprocessing pipeline used during data transformation.
train.csv and test.csv: Train and test datasets after splitting.

Contributing
If you would like to contribute to this project:
Fork the repository.
Create a new branch (git checkout -b feature-branch).
Commit your changes (git commit -m 'Add new feature').
Push to the branch (git push origin feature-branch).
Open a pull request.

License
This project is licensed under the terms of the LICENSE file.
