# MindSense – Sentiment Analysis for Mental Health 🧠💬

This project applies **Natural Language Processing (NLP)** to analyze and classify sentiments related to different mental health conditions. The aim is to extract meaningful insights from textual data and develop models capable of identifying mental health patterns based on linguistic cues.

---

## 📊 Dataset

* **Source**: [Kaggle Dataset](https://www.kaggle.com/datasets/suchintikasarkar/sentiment-analysis-for-mental-health/data)

* **Class Distribution**:

  * Normal: 16,343
  * Depression: 15,404
  * Suicidal: 10,652
  * Anxiety: 3,841
  * Bipolar: 2,777
  * Stress: 2,587
  * Personality Disorder: 1,077

---

## 🔎 Exploratory Data Analysis (EDA)

**Main Steps:**

1. **Word Frequency Analysis**

   * Plotted the top 15 most frequent terms (after stop word removal) for each condition.
   * Example takeaways:

     * *Anxiety*: Frequent words included *anxiety*, *feel*, *know*.
     * *Normal*: Positive terms like *good* and *day* dominated.
     * *Suicidal*: Keywords such as *want*, *life*, *anymore* reflected distress.

2. **Condition-specific Word Patterns**

   * Shared terms like *feel*, *like*, *want* appeared across multiple conditions.
   * Unique linguistic markers stood out (e.g., *anxiety* in Anxiety, *depression* in Depression).

3. **Word Clouds**

   * Generated visual word clouds for each class, highlighting emotional and contextual focus:

     * *Depression*: *feel*, *life*, *depression*
     * *Stress*: *stress*, *help*, *work*
     * *Suicidal*: *want*, *life*, *die*

---

## 🧹 Data Preprocessing

1. **Cleaning Steps**:

   * Tokenization
   * Removal of punctuation, special characters, and stop words
   * Lowercasing
   * Stemming/Lemmatization

2. **Balancing Techniques**:

   * Applied **data augmentation** (synonym replacement, insertion, random swaps).
   * Combined **TF-IDF features** with **SMOTE** to handle class imbalance.

---

## 🤖 Modeling and Results

### Approaches Tested:

1. **TF-IDF + SMOTE + Traditional Classifiers**

   * Models such as **XGBoost** performed well.
   * Achieved **74% accuracy** with improved F1 scores, especially for minority classes.

2. **Word2Vec + Bi-LSTM**

   * Leveraged embeddings with a **Bidirectional LSTM**.
   * Outperformed other models with **76% accuracy** and higher F1 scores for underrepresented conditions.

3. **Additional Models**

   * CNN and vanilla LSTM were explored but underperformed compared to Bi-LSTM.

---

## 🌟 Key Insights

* **Linguistic Indicators**:

  * Stress-related text often mentioned *help* and *work*.
  * Suicidal tendencies were strongly tied to words like *life* and *anymore*.

* **Feature Importance**:

  * Specific keywords emerged as strong predictors for particular conditions.

* **Challenges**:

  * Significant effort was required to mitigate class imbalance.
  * Computational limitations restricted experiments with larger deep learning models.

---

## 🚀 Potential Applications

* **Early Detection**: Identify warning signs of mental health struggles in user-generated text.
* **Crisis Intervention**: Automatically flag urgent phrases (e.g., *suicide*, *kill*) for timely support.
* **Emotion Profiling**: Track emotional trends and sentiment shifts across different conditions.

---

## 🛠️ Tools & Technologies

* **Libraries**:

  * Data: `pandas`, `numpy`
  * Visualization: `matplotlib`, `seaborn`
  * ML/DL: `sklearn`, `XGBoost`, `LightGBM`, `CatBoost`, `imblearn`
  * NLP: `gensim` (Word2Vec), `TensorFlow`, `Keras`

* **Techniques**:

  * Text preprocessing (tokenization, lemmatization, stop word removal)
  * Data balancing (SMOTE, augmentation)
  * Visualization (word clouds, frequency plots)

---

## 🖋️ Conclusion

This project highlights how NLP can provide valuable insights into mental health conditions through language analysis. By combining **EDA**, **feature engineering**, and **robust modeling**, it demonstrates how text-based signals can be leveraged for **early detection** and **intervention support** in mental health care.

---
