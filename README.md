

# Financial News Sentiment Analysis: N-gram Generation and Analysis
This repository contains a Python script, ngrams.py, that performs n-gram analysis on a dataset of financial news headlines. The script preprocesses the text, generates unigrams, bigrams, and trigrams, and then analyzes their frequency. It also builds and evaluates language models using different smoothing and interpolation techniques.

#Prerequisites
To run this script, you'll need to have Python and the following libraries installed. You can install them using pip:

# Bash

pip install pandas scikit-learn nltk kagglehub matplotlib wordcloud
Additionally, the script uses the NLTK library, which requires downloading specific data corpora. The script includes code to automatically download these, but if you encounter any issues, you can download them manually by running the following in a Python interpreter or a separate script:

Python

import nltk
nltk.download('stopwords')
nltk.download('punkt')
How to Run the Script
Download the script: Ensure you have the ngrams.py file.

Run from your terminal: Open a terminal or command prompt, navigate to the directory where you saved the file, and run the script using the Python interpreter:

Bash

python ngrams.py
What the Script Does
The script performs the following tasks in order:

Data Acquisition: It automatically downloads a financial news dataset from Kaggle using the kagglehub library.

Data Preprocessing: It cleans the text data by:

Adding appropriate column headers.

Converting all text to lowercase.

Tokenizing the sentences and words using NLTK.

Removing common English stop words (e.g., "the," "a," "is").

N-gram Generation: It generates unigrams (single words), bigrams (two-word phrases), and trigrams (three-word phrases) from the preprocessed text.

Frequency Analysis & Visualization: The script calculates the frequency of each n-gram and displays the top 10 most common ones. It also generates bar plots and a word cloud to visualize the distribution of these n-grams.

Language Modeling: It splits the dataset into training and testing sets to build and evaluate predictive language models.

Perplexity Calculation: The script calculates the perplexity of the models, a metric for how well a probability model predicts a sample. It demonstrates how Laplace smoothing helps handle unseen words and how linear interpolation can combine models for improved performance.

After running the script, you'll see various outputs printed to the console, including the dataframes, frequency counts, and perplexity scores. The script will also generate and display several plots in separate windows.
