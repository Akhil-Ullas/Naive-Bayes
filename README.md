📌 What is Naive Bayes and Why is it Called “Naive”?

Naive Bayes is a probabilistic classifier based on Bayes’ Theorem.
It predicts the class with the highest posterior probability.

It is called “Naive” because it assumes that all features are:

conditionally independent given the target class

This assumption is unrealistic in many real-world datasets — especially text — yet Naive Bayes still performs strongly due to:

• simplicity
• fast computation
• stability on sparse, high-dimensional data

This makes it a powerful and practical baseline model.

📌 Variants of Naive Bayes Explored

🔹 Gaussian Naive Bayes (GaussianNB)
Used for continuous numeric features that follow a normal distribution
Common in medical & sensor-based datasets.

It models each feature using a Gaussian (bell-curve) distribution within each class.

🔹 Multinomial Naive Bayes (MultinomialNB)
Best suited for text classification with:

• Count Vectorizer
• Bag-of-Words
• word frequency features

It models word occurrence counts, making it ideal for:

• spam filtering
• sentiment analysis
• document classification

This was the most effective model across most text datasets I worked on.

🔹 Bernoulli Naive Bayes (BernoulliNB)
Works with binary features such as:

• word present vs not present
• keyword indicators
• binary attribute flags

Useful when word frequency matters less than occurrence.

📌 Role of Count Vectorizer

Count Vectorizer converts text into numeric feature vectors by:

• mapping tokens to vocabulary indices
• representing documents as word-occurrence counts

This enabled scalable bag-of-words text representation across projects.

📌 Pipeline Integration

ML Pipelines were used to:

• combine preprocessing + feature extraction + model training
• avoid manual repetition
• prevent data leakage
• ensure clean and reproducible experiments

Typical workflow:

Text Preprocessing → Count Vectorizer → Naive Bayes Model

This strengthened my understanding of production-ready ML workflows.

✔ Advantages of Naive Bayes

• Extremely fast to train and predict
• Performs well on high-dimensional text data
• Requires minimal training data
• Robust to irrelevant features
• Strong baseline classifier

✘ Disadvantages of Naive Bayes

• Independence assumption is rarely realistic
• Can struggle when features are highly correlated
• Probability estimates may be poorly calibrated
• Sensitive to zero-frequency terms without smoothing
