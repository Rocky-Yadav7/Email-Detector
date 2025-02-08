# Email Spam/Ham Classification

## Overview
This project is an implementation of SMS spam classification using the Naïve Bayes algorithm in R. The model is trained to distinguish between spam and non-spam (ham) messages based on text preprocessing and machine learning techniques.

## Dataset
The dataset used is `sms_spam.csv`, which consists of SMS messages labeled as either spam or ham. The `type` column indicates the label, and the `text` column contains the SMS content.

## Prerequisites
Ensure you have R installed on your system. You will also need the following R packages:
- `tm`
- `SnowballC`
- `wordcloud`
- `e1071`
- `gmodels`

You can install these packages using:
```r
install.packages("tm")
install.packages("SnowballC")
install.packages("wordcloud")
install.packages("e1071")
install.packages("gmodels")
```

## Steps

### 1. Load Data
- Read the CSV file.
- Convert the `type` column to a factor.

### 2. Text Preprocessing
- Convert text to lowercase.
- Remove numbers, stopwords, and punctuation.
- Apply stemming.
- Strip extra whitespace.

### 3. Create Document-Term Matrix
- Generate a `DocumentTermMatrix`.
- Split the dataset into training and testing sets.

### 4. Feature Selection
- Identify frequently occurring words.
- Convert word counts into categorical values (Yes/No).

### 5. Train Naïve Bayes Classifier
- Train the classifier using the `naiveBayes` function from the `e1071` package.
- Predict on test data.

### 6. Evaluate Model
- Generate a confusion matrix.
- Compute accuracy.

## Running the Code
Execute the script in RStudio or an R environment:
```r
source("sms_spam_classifier.R")
```

## Output
- A word cloud of frequent words.
- Confusion matrix.
- Accuracy percentage of the classifier.

## Results
The model provides an accuracy score displayed in the console, indicating its performance in classifying SMS messages as spam or ham.

## License
This project is open-source and available under the MIT License.

