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

## **Analysis**
We used two interesting techniques: word clouds and ABSA to analyze tweets. A **word cloud** is a visual tool that shows the most common words in our dataset in a fun, easy-to-read way. The more often a word appears in the tweets, the bigger and bolder it shows up in the cloud. This gives us a quick glance at what topics are most talked about. On the other hand, **ABSA** helps us dig deeper by not just looking at whether tweets are positive or negative, but also understanding what specific aspects of the products people are talking about:

<img width="1788" alt="Screenshot 2024-01-26 at 4 00 51 PM" src="https://github.com/Yiyi-Luo/Project-IV-TweetSense-Analytics-Unveiling-Consumer-Sentiments-on-Apple-Google-Products/assets/149438809/79494388-dd0c-4989-995a-fa29ca4dbdde">

Our result presents a visual breakdown of key terms commonly found in positive and negative reviews about Apple and Google products. For Apple, positive mentions frequently highlight the "Apple Store", "Pop up" and "Novelty," suggesting an appreciation for the shopping experience and new features. On the flip side, negative Apple-related reviews often focus on specific product features like "iPhone Battery" and "iPad Design," indicating areas where consumers might be experiencing dissatisfaction.

For Google, positive reviews are associated with services like "Google Map" and the innovation linked with "Circle/New Social”; Meanwhile, negative sentiments are expressed with terms like "Bing" and "Circle," which might relate to less favorable comparisons within Google's product ecosystem.

<img width="1245" alt="Screenshot 2024-01-26 at 4 02 08 PM" src="https://github.com/Yiyi-Luo/Project-IV-TweetSense-Analytics-Unveiling-Consumer-Sentiments-on-Apple-Google-Products/assets/149438809/8229ccf7-6f6a-4c5b-8e94-8d8a4f3779d7">

## **Recommendations:**

Based on the results, we came up with three recommendations:

**1. Enhance Product Features:** For Apple, addressing the negative feedback on "iPhone Battery" and "iPad Design" should be a priority;

   
**2. Address Brand Confusion:** The negative association with "Bing" in Google's context could indicate confusion due to comparison with Microsoft's search engine. It's crucial to clarify brand messaging and differentiate Google's offerings more clearly;

	
**3. Innovate and Communicate:** The mixed sentiments around Google's "Circle/New Social" suggest both interest and skepticism. Google should focus on innovating in the social space and effectively communicate the benefits of its social platforms to turn negativity into positivity.


