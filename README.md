# Machine Learning Project: Student Performance Analysis and Prediction

This project focuses on analyzing and predicting student performance based on various factors, using machine learning algorithms to gain insights and predict future performance trends.

## Features
- Data preprocessing and visualization
- Exploratory data analysis (EDA)
- Model building and evaluation
- Performance prediction

## Tools and Technologies
- **Python**
- **Pandas**
- **NumPy**
- **Scikit-learn**
- **Matplotlib**
- **Seaborn**
- **CatBoost** (specific information stored in `catboost_info`)

## Data
The dataset used in this project includes various student-related features such as demographic factors, social influences, and academic performance indicators.

## Project Structure
The project is organized into the following directories:

```plaintext
notebook/
    catboost_info/               # Information related to CatBoost models
    data/
        1. EDA STUDENT PERFORMANCE.ipynb  # Notebook for Exploratory Data Analysis (EDA)
        2. MODEL TRAINING.ipynb           # Notebook for Model Training
src/
    components/                   # Reusable components for the project
    logs/                         # Log files for tracking execution
    pipeline/
        __init__.py               # Initialization for the pipeline package
        predict_pipeline.py       # Pipeline for model prediction
        train_pipeline.py         # Pipeline for training the model
    __init__.py                   # Initialization for the main src package
    exception.py                  # Custom exception handling
    logger.py                     # Logging setup
    utils.py                      # Utility functions
templates/
    home.html                     # HTML file for the home page
    index.html                    # HTML file for index page
venv/                             # Virtual environment files (not tracked in Git)
.github/
    workflows/
        main.yaml                 # Workflow configuration for CI/CD
artifacts/
    model.pkl                     # Pickled model file
    preprocessor.pkl              # Pickled preprocessor file
    raw.csv                       # Raw data file
    test.csv                      # Test data file
    train.csv                     # Training data file
.gitignore                        # Files and directories to be ignored by Git
app.py                            # Main application entry point
Dockerfile                        # Dockerfile for containerizing the application
README.md                         # Project documentation
requirements.txt                  # Python dependencies
setup.py                          # Setup script for packaging
```

## Installation

### 1. Create a Conda Environment
Ensure you have Conda installed. Then, create and activate a conda environment with Python version 3.8:

```bash
conda create --name myenv python=3.8
conda activate myenv
```

### 2. Clone the Repository
Clone the repository from GitHub:

```bash
git clone https://github.com/Shayan704/mlproject.git
cd mlproject
```

### 3. Install Required Packages
Use the following command to install the dependencies:

```bash
pip install -r requirements.txt
```

## Usage

- **Data Exploration and Model Training**: Open and run the Jupyter notebooks provided in the `notebook` directory to explore the data and train the models.
- **Model Deployment**: To deploy the models, use Flask and Gunicorn. You can set up a server to serve your models for predictions.

### Run the Application
Use the following command to run the project:

```bash
python app.py
```

## CI/CD with GitHub Actions

This project uses CI/CD pipelines and is built in a completely modular way. It uses GitHub Actions for continuous integration and deployment. To enable this, add the following GitHub secrets to your repository:

- `DOCKERHUB_PASSWORD`
- `DOCKERHUB_USERNAME`
- `RENDER_API_KEY`
- `RENDER_SERVICE_ID`

These secrets are required to ensure the CI/CD pipeline can build, test, and deploy your application automatically.
```