# Twitter-Sentimental-Analysis
It contains 1,600,000 tweets extracted using the twitter api . The tweets have been annotated (0 = negative, 4 = positive) and they can be used to detect sentiment .


1. Setup (Part 1):

Imports libraries for text processing, visualization, and machine learning.
Establishes the environment for NLP tasks like data cleaning, visualization, and classification.

2. Data Loading & Preprocessing (Parts 2 & 3):

Loads data from a CSV file, sets encoding, and renames columns.
Extracts text and sentiment labels.
Defines dictionaries for emojis and stop words for further processing.

3. Text Preprocessing Function (Part 4):

Takes a text list as input and performs various cleaning steps:
Lowercases text.
Replaces URLs, emojis (with meanings), user mentions, and non-alphabetic characters.
Reduces repeated characters (e.g., "haaaaappy" becomes "happy").
Applies lemmatization (converts words to their base form).

4. Preprocessing Time Measurement (Part 5):

Calculates the time taken for text preprocessing using the defined function.

5. Word Cloud Visualization (Parts 6 & 7):

Generates separate word clouds for positive and negative sentiment text after preprocessing.
Uses WordCloud library with customizations like maximum words, size, and color distribution.

6. Train-Test Split (Part 8):

Splits preprocessed text data and sentiment labels into training (95%) and testing (5%) sets for model evaluation.

7. TF-IDF Vectorizer (Part 9):

Creates a TF-IDF vectorizer to represent text data numerically.
Considers unigrams and bigrams (single and two-word combinations).
Limits features to 500,000 for efficiency.
Fits the vectorizer to the training data.

8. Data Transformation (Part 10):

Transforms both training and testing text data into TF-IDF feature vectors using the fitted vectorizer.

9. Model Evaluation Function (Part 11):

Takes a machine learning model and evaluates it using the test data.
Prints classification report (precision, recall, F1-score) and confusion matrix for performance visualization.

10. Bernoulli Naive Bayes Model (Part 12):

Initializes and trains the model with smoothing parameter for handling unseen words.
Evaluates the model using the defined evaluation function.

11. Logistic Regression Model (Part 13):
Initializes and trains the model with regularization and maximum iterations parameters.
Utilizes all available processors for faster training.
Evaluates the model using the defined evaluation function.

12. Model Persistence (Part 14):
Saves the trained vectorizer and models (Logistic Regression) using pickle serialization for later use.

13. Prediction Functions (Part 15):
Defines functions to load saved models and predict sentiment for new text data.
The predict function preprocesses the input text, uses the model for prediction, and returns a DataFrame with text and predicted sentiment.
Demonstrates loading models and predicting sentiment for sample text (requires uncommenting specific lines).
