# Amazon-Alexa-Reviews

This project involves sentiment analysis of Amazon Alexa reviews, aiming to classify each review as positive or negative using a machine learning model. The steps involved include data loading, cleaning, exploratory data analysis (EDA), preprocessing, and building machine learning models.

### 1. **Exploratory Data Analysis (EDA)**
   - **Dataset Description**: The dataset contains 3150 records with 5 columns: `rating`, `date`, `variation`, `verified_reviews`, and `feedback`. The `feedback` column is binary, where `1` represents positive feedback, and `0` represents negative feedback.
   - **Null Values**: The dataset had a single null record, which was dropped.
   - **Length Analysis**: A new feature, `length`, was added to capture the length of the review text, which shows that reviews vary significantly in length.

### 2. **Sentiment Distribution**
   - **Rating Analysis**: 72.57% of the reviews gave a 5-star rating, while only 5.11% gave a 1-star rating.
   - **Feedback Analysis**: 91.84% of the reviews have positive feedback (`feedback = 1`), and 8.16% have negative feedback (`feedback = 0`). This shows a heavy imbalance in the dataset.
   - **Variation Analysis**: The dataset includes different Amazon Alexa product variations. The most reviewed product was the "Black Dot" variation, while less common variations like "Walnut Finish" had few reviews.

### 3. **Visualizing the Data**
   - **WordClouds**: Word clouds were generated for both positive and negative reviews. Positive reviews contained words like "amazing", "enjoying", "great", etc., while negative reviews had words like "garbage", "pointless", "poor", etc.
   - **Bar Plots**: Bar plots were used to visualize the distribution of ratings, feedback, and variations.

### 4. **Text Preprocessing**
   The text data (`verified_reviews`) was preprocessed by:
   - Removing non-alphabetical characters.
   - Converting to lowercase and removing stopwords.
   - Applying stemming using the Porter Stemmer to reduce words to their root form.
   - Creating a Bag of Words representation using `CountVectorizer`.

### 5. **Model Building**
   After preprocessing, machine learning models were built using the processed text features (`X`) and the feedback labels (`y`).

#### **Train-Test Split**:
   - The dataset was split into training and test sets with a 70-30 ratio.

#### **Classification Models**:
   Various classification models could be tested:
   - **RandomForestClassifier**: A robust ensemble model that works well with text data.
   - **DecisionTreeClassifier**: Simple yet effective for smaller datasets.
   - **XGBClassifier**: A powerful model often used for text-based classification.

Each model can be evaluated based on its **accuracy**, **confusion matrix**, and other relevant metrics like precision and recall.

This process can help build a robust sentiment analysis model for classifying Amazon Alexa reviews as either positive or negative based on user feedback.
