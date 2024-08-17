# Fake News Detection

## Introduction

In an era where information is widely accessible, distinguishing between reliable and unreliable news has become increasingly important. The spread of misinformation, often referred to as "fake news," poses significant risks to public discourse and trust in media. This project aims to tackle this problem by developing a machine learning model that can identify fake news articles with high accuracy.

## Dataset Description

The dataset used for this project contains news articles labeled as either "real" or "fake." The dataset includes the following attributes:
- **id**: Unique identifier for each news article.
- **title**: The title of the news article.
- **author**: The author of the news article.
- **text**: The main content of the article, which might be incomplete.
- **label**: A binary label indicating the article's reliability (1 for unreliable/fake, 0 for reliable/real).

## Project Workflow

### 1. Data Preprocessing
   - Merging the title and text columns into a single body column.
   - Cleaning the text data by removing URLs, special characters, and stopwords.
   - Converting the text data to lowercase and applying lemmatization.

### 2. Feature Extraction
   - Using TF-IDF Vectorization to convert the cleaned text into numerical features.

### 3. Model Training
   We experimented with the following models:
   1. **Decision Tree Classifier**
   2. **Passive Aggressive Classifier**
   3. **XGBoost Classifier**
   4. **Random Forest Classifier**
   5. **Neural Network (Feedforward)**

### 4. Model Evaluation
   The models were evaluated based on their accuracy. The results are summarized below:

| Model                  | Accuracy (%) |
| ---------------------- | ------------ |
| Decision Tree          | 80.35        |
| Passive Aggressive     | 93.45        |
| XGBoost                | 86.90        |
| Random Forest          | 90.21        |
| Neural Network         | 93.53        |

### 5. Predictive System
   A function was created to predict whether a given news article is real or fake based on the trained model.

### 6. Model Persistence
   The best-performing model and the TF-IDF vectorizer were saved using `pickle` for future use.

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone <repository-url>
