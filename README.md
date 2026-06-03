# Movie-Review-Sentiment-Analysis
Predictive text analysis project using IMDB movie review data to identify whether reviews are most likely positive or negative. The project uses Python to perform tokenization, TF-IDF vectorization, Logistic Regression, and Random Forest classification to analyze review language, compare model performance, and uncover key sentiment drivers.

## Project Overview

This project analyzes text data from IMDB movie reviews to predict whether a review expresses positive or negative sentiment. The dataset contains written movie reviews and sentiment labels connected to each review. The main objective of this project is to build a machine learning model that can classify reviews into two groups: 0 = Negative Review 1 = Positive Review. By identifying the words and patterns most associated with positive and negative sentiment, this analysis can help entertainment companies, streaming platforms, and review websites better understand audience feedback. 

## Business Problem

Entertainment companies and movie platforms often receive large amounts of written customer feedback. Without a clear way to classify reviews as positive or negative, it can be difficult to quickly understand audience opinion. Manually reading thousands of reviews is slow, inefficient, and difficult to scale. This project addresses the following question:

Can we use movie review text to predict whether a review is positive or negative?

The insights could help the company: Identify positive audience reactions Identify negative audience reactions Summarize large amounts of customer feedback Reduce manual review reading Better understand audience satisfaction Support movie recommendation and content decisions

## Dataset Description

The dataset contains review-level information from IMDB. The variables include movie review text and a sentiment label. Key fields include: Review, Sentiment The review column contains the written customer review. The sentiment column indicates whether the review is positive or negative. The target variable is Sentiment, which was converted into a numeric value where 0 = negative and 1 = positive.

## Data Cleaning and Preprocessing

Before modeling, the dataset was cleaned and prepared for sentiment analysis. The preprocessing steps included: Checked the dataframe structure Checked for missing values Checked for duplicate reviews Removed duplicate reviews Converted sentiment labels into numeric values Cleaned the review text Removed HTML tags Removed punctuation and numbers Converted text to lowercase Tokenized each review into individual words Created token count and review length features Separated the data into features and target variable Split the data into training and testing sets Used TF-IDF vectorization to convert text into numeric features Tokenization was used because machine learning models cannot directly understand full sentences. TF-IDF was used because it helps identify words that are more important to each review instead of treating every word equally.

## Methodology

Loaded and reviewed the IMDB dataset Cleaned the review text and checked the data structure Removed duplicate reviews Converted positive and negative labels into numeric values Tokenized the cleaned review text Created basic text features such as token count and review length Reviewed basic correlations between sentiment and text features Analyzed the most common tokens after cleaning Split the data into training and testing sets Used TF-IDF vectorization to prepare the text for modeling Built a Logistic Regression classification model Built a Random Forest classification model Compared both models using accuracy, ROC-AUC, confusion matrix, and classification report Analyzed important words from Logistic Regression and Random Forest to identify key sentiment drivers

## Models Used

### Logistic Regression

Logistic Regression was used as a baseline model because it is simple, interpretable, and effective for binary classification problems. Since the target variable is whether a review is positive or negative, Logistic Regression provides a clear starting point for understanding how certain words relate to sentiment.

### Random Forest Classifier

Random Forest was used as the second machine learning model because it can capture more complex relationships in the data. Unlike Logistic Regression, which assumes a more direct relationship between features and the target, Random Forest uses multiple decision trees to identify patterns that may not be obvious through a simpler model.

## Model Comparison

After training both models, their performance was compared using several classification metrics: Accuracy: Measures the percentage of correct predictions Confusion Matrix: Shows correct and incorrect predictions for each class Classification Report: Provides precision, recall, and F1-score ROC-AUC: Measures how well the model separates positive and negative reviews Using both models allowed the project to compare a simpler, more interpretable model against a more flexible machine learning model. This comparison helps answer not only whether movie review sentiment can be predicted, but also which model provides better performance for this type of text classification problem.

## Key Objective

Which reviews are most likely to be positive or negative, and which model best predicts movie review sentiment?

## Business Value

A company could use this type of prediction model to: Classify customer reviews faster Understand audience reaction at scale Identify common positive and negative language Reduce manual review reading Improve customer feedback analysis Support recommendation systems Compare model approaches before choosing one for business use

## Limitations

This project is based on review text, so the results should be interpreted carefully. Other limitations include: The model does not include movie genre, release year, star rating, reviewer history, or box office data Text cleaning may remove some context from the original review Sarcasm and complex language can be difficult for models to understand Random Forest can be slower than Logistic Regression when working with large text datasets The project uses a sample of the full dataset to keep the notebook easier and faster to run

## Conclusion

This project uses IMDB movie review data to predict whether a review is positive or negative. We cleaned the data, removed duplicate reviews, converted sentiment labels into numbers, tokenized the review text, and used TF-IDF to convert words into numerical features. We then built two models: Logistic Regression and Random Forest. After comparing them, we used the results to see which model predicted sentiment better and what words seemed most connected to positive and negative reviews.

Overall, this project helps show how data science can be used to analyze written text and turn customer opinions into useful insights.
