# Sentiment Analysis of Customer Feedback

## Description

This project performs sentiment analysis on customer feedback using a machine learning model. The goal is to classify feedback as either "Positive" or "Negative". The project uses a Logistic Regression model trained on a dataset of customer reviews.

## Dataset

The dataset used for this project is `sentiment-analysis.csv`. It contains the following columns:

* **Text**: The customer feedback text.
* **Sentiment**: The sentiment of the feedback (Positive/Negative).
* **Source**: The source of the feedback (e.g., Twitter, Yelp).
* **Date/Time**: The date and time of the feedback.
* **User ID**: The ID of the user who provided the feedback.
* **Location**: The location of the user.
* **Confidence Score**: The confidence score of the sentiment.

For this project, only the `Text` and `Sentiment` columns are used.

## Installation

To set up the environment and run this project, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone <your-repository-url>
    cd <your-repository-name>
    ```

2.  **Create and activate a virtual environment (optional but recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Download NLTK data:**
    The first time you run the notebook, it will download the necessary `punkt` and `stopwords` data from NLTK.

## Usage

To run the sentiment analysis, open and run the `sentiment_analysis.ipynb` notebook in Jupyter Notebook or JupyterLab.

The notebook is structured as follows:
1.  **Loading Data**: Loads and cleans the `sentiment-analysis.csv` dataset.
2.  **Preprocessing Text**: Cleans and preprocesses the text data by removing punctuation, converting to lowercase, and removing stopwords.
3.  **Extracting Features with TF-IDF**: Converts the text data into numerical features using TF-IDF vectorization.
4.  **Training Logistic Regression Model**: Splits the data into training and testing sets and trains a Logistic Regression model.
5.  **Evaluating the Model**: Evaluates the model's performance using accuracy, a classification report, and a confusion matrix.
6.  **Making Predictions on New Feedback**: Provides a function to predict the sentiment of new, unseen text.

## File Structure

```
├── sentiment_analysis.ipynb      # The main Jupyter Notebook for the analysis
├── sentiment-analysis.csv        # The dataset with customer feedback
├── requirements.txt              # A list of Python packages required to run the project
├── .gitignore                    # Specifies which files to ignore in the repository
└── README.md                     # This README file
```
