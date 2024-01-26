### **Project-IV-TweetSense-Analytics-Unveiling-Consumer-Sentiments-on-Apple-Google-Products**
**Yiyi Luo**

## **Overview and Business Understanding**

This project focuses on evaluating social media  sentiment towards Apple and Google products, aiming to deliver actionable insights for tech companies and marketers to refine marketing approaches, product development and brand strategy.

**Phase I:** Employ machine learning techniques to develop models capable of discerning sentiments in tweets;

**Phase II:** Leverage word clouds and Aspect-Based Sentiment Analysis (ABSA) to identify the specific aspects associated with these sentiments.


## **Data Understanding and Preparation**

1. **Data Selection and Cleaning**: In our initial basic cleaning: we combined, renamed some columns and dropped null values;

2. **Feature Engineering and Preprocessing**: Applied OneHotEncoding to transform categorical data for analytical compatibility; Utilized 'dropna' technique to maintain data integrity and reliability;

3. **Addressing Data Imbalance**: Instead of a binary view, we categorized sentiments into three groups: positive, neutral, and negative. This approach is more aligned with the varied nature of tweets. However, it could make achieving accurate results become more complex. We recognized and addressed the imbalance in the 'Emotion Type' target variable; Employed class weights and KMeanSMOTE strategies to achieve a more balanced dataset for unbiased insights;

4. **Preparation for Predictive Modeling**: We performed URL Removal, Mention Removal, Tokenization, Lowercasing, Handling Negations, Stopword Removal, Part-of-Speech Tagging, Lemmatization and Aggregating Processed Words to preprocess the data for our NLP model training and further analysis.


## **Modeling**
Trained some **traditional machine learning models** (such as: **SVM, Random Forest, Naive Bayes and XGBoost**) from scratch, but also utilized some pre-trained deep learning models (such as: **BERTweet, RoBERTa, ERNIE, BERT-large, DeBERTa, XLNet, ELECTRA**). These deep learning models have been developed through extensive training, a significant investment in computational resources, large-scale data input, and considerable human effort. 

Not surprisingly, the pre-trained Deep learning models showed remarkable performance, outshining the basic models. Our best model—**BERTweet**, designed specifically for analyzing tweets, excels in this project due to its ability to handle the informal language found in social media.

<img width="804" alt="Screenshot 2024-01-26 at 3 51 21 PM" src="https://github.com/Yiyi-Luo/Project-IV-TweetSense-Analytics-Unveiling-Consumer-Sentiments-on-Apple-Google-Products/assets/149438809/71512dbe-fde3-4f48-8235-f614e4a244a5">

**Our best model—BERTweet**, designed specifically for analyzing tweets, excels in this project due to its ability to handle the informal language found in social media. Given the challenge posed by the imbalanced nature of our dataset, BERTweet's results are particularly noteworthy. 

<img width="697" alt="Screenshot 2024-01-26 at 3 55 12 PM" src="https://github.com/Yiyi-Luo/Project-IV-TweetSense-Analytics-Unveiling-Consumer-Sentiments-on-Apple-Google-Products/assets/149438809/2da14a5a-2e74-4adb-a388-0295535200e8">

The model's ability to accurately identify and classify the minority class in the data is commendable. This is reflected in the impressive **recall and F1 scores**: These metrics are crucial in cases where catching every instance of the minority class is important, and BERTweet's proficiency here demonstrates its effectiveness in dealing with skewed data distributions.




