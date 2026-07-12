# Spam Detection in SMS and Email using Machine Learning

## Machine Learning for Cybersecurity: Threat & Spam Detection

### Project Overview
This project demonstrates the application of Machine Learning (ML) to enhance cybersecurity postures. In a modern SOC (Security Operations Center), automation is key to handling the massive volume of alerts. This project explores two critical use cases:
1. **Network Intrusion Analysis**: Using statistical validation and advanced imputation to clean noisy network logs and prepare them for anomaly detection.
2. **SMS Phishing (Smishing) Classification**: Implementing a Natural Language Processing (NLP) pipeline to identify malicious messages using Naive Bayes and Grid Search optimization.

### Tools Used
- Python
- Jupyter Notebook
- Git

### Tech Stack Used
- Machine Learning (Classification)
- Natural Language Processing (NLP)
- Data Engineering & Preprocessing

### Libraries Used
- **Pandas & NumPy**: For data manipulation, numerical operations, and transformation.
- **Scikit-Learn**: For feature imputation (KNN, SimpleImputer), one-hot encoding, model building (Multinomial Naive Bayes), pipelines, and hyperparameter tuning (GridSearchCV).
- **NLTK (Natural Language Toolkit)**: For text tokenization, stopword removal, and stemming (PorterStemmer).
- **Joblib**: For model persistence, serialization, and deployment readiness.
- **Regular Expressions (`re`)**: For advanced text cleaning, IP validation, and filtering.
- **Python Standard Libraries (`requests`, `zipfile`, `io`, `os`)**: For automated external data acquisition and system operations.

### Techniques Used

#### Part 1: Network Threat Data Engineering
- **Statistical Validation**: Rigorous data gatekeeping including Regex-based IP validation, logic-based port validation, protocol whitelisting, data integrity checks, and targeted label cleaning.
- **Advanced Feature Imputation**: Utilization of K-Nearest Neighbors (KNN) and Median imputation to intelligently reconstruct missing/corrupted data gaps.
- **Transformation & Vectorization**: One-hot encoding of categorical networking protocols and logarithmic scaling (`np.log1p`) to mitigate skewness from large traffic spikes (e.g., potential DDoS indicators).

#### Part 2: NLP for SMS Phishing Detection
- **Text Preprocessing Pipeline**: Lowercasing and selective character filtering to remove noise while preserving high-signal phishing indicators like currency symbols (`$`) and exclamation marks (`!`).
- **Tokenization & Stopword Removal**: Breaking down strings into distinct tokens and removing common words (e.g., "the", "is") to prioritize high-intent keywords.
- **Stemming**: Reducing words to their root or base form for uniform feature extraction.
- **Feature Extraction (Bag of Words)**: Generating a sparse numerical matrix with `CountVectorizer` and integrating Bigrams to retain semantic context (e.g., "account locked").
- **Model Selection & Optimization**: Training a Multinomial Naive Bayes model tailored for discrete word counts, rigorously optimized using Grid Search with 5-fold cross-validation.
- **Probability Scoring**: Outputting probability metrics (Confidence Levels) rather than strict binaries for more nuanced SOC alerting.

### Dataset Used
In this project dataset was synthetic dataset from HackTheBox platform.

**Author:** Engr. Hammad Khurshid
