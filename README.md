# Stylometric Analysis of Children’s Literature (1700–Present)

##  Overview

This project explores how the **language, style, and themes** in children’s literature have evolved over the past three centuries. Using 15 iconic books from the 18th to 21st century, we apply **natural language processing (NLP)** and **stylometric techniques** to analyze changes in:

- Sentence structure and complexity  
- Vocabulary richness and readability  
- Emotional and moral tone  
- Thematic trends (via topic modeling)  
- Writing style classification using machine learning

Our core hypothesis: Over time, children’s literature has become simpler, more emotionally expressive, and increasingly inclusive.

---

##  Research Question

> How has children’s literature evolved in terms of writing style, vocabulary usage, and thematic content between 1700 and today?

---

##  Project Structure

├── data/ # Raw and cleaned text files
├── notebooks/ # Jupyter notebooks for analysis
│ ├── 01_data_preprocessing.ipynb
│ ├── 02_feature_extraction.ipynb
│ ├── 03_visualization.ipynb
│ ├── 04_topic_modeling.ipynb
│ └── 05_machine_learning.ipynb
├── output/ # Visualizations, model results
├── lexicons/ # Emotion and morality word lists
├── report/ # Final paper and presentation slides
├── requirements.txt # Python dependencies
└── README.md # 

---

##  Corpus

We selected 15 culturally significant children’s books across 4 historical periods:

| Period        | Sample Books                                         |
|---------------|------------------------------------------------------|
| 1700–1799     | *A Little Pretty Pocket-Book*, *Goody Two-Shoes*     |
| 1800–1899     | *Alice's Adventures in Wonderland*, *Heidi*          |
| 1900–1999     | *Charlie and the Chocolate Factory*, *Matilda*       |
| 2000+         | *Wonder*, *Coraline*                                 |

---

##  Tools & Libraries

- **Python 3.9+**
- `NLTK` – Tokenization, POS tagging, sentiment analysis
- `textstat` – Readability metrics (Flesch, Dale–Chall)
- `scikit-learn` – TF-IDF, LDA, classification models
- `matplotlib`, `seaborn` – Visualizations
- `pandas`, `numpy` – Data manipulation

---

##  Methodology

### Stylometric Features
We extracted key linguistic and readability features:
- **Word-level:** avg. word length, lexical diversity, moral/emotional word ratios
- **Sentence-level:** avg. sentence length, complex/short/long sentence ratios
- **Readability scores:** Flesch Reading Ease, Dale–Chall
- **Syntactic style:** function word ratio, adjective/noun/verb frequency

### Topic Modeling
- Used **Latent Dirichlet Allocation (LDA)** to extract common themes
- Tracked dominant themes and changes across eras

### Machine Learning Classification
- Trained **SVM**, **Logistic Regression**, and **Random Forest** models to classify books by era based on stylistic features
- Achieved **73% accuracy** using Linear SVM with 5-fold cross-validation

---

##  Key Findings

- **Simplification Over Time:** Sentences and words have become shorter and simpler, improving readability.
- **Emotional > Moral:** Use of moral words has declined; emotional content is more stable and expressive.
- **Modern Themes:** Shift from morality and obedience to identity, imagination, empathy, and belonging.
- **Distinct Eras:** Low cosine similarity scores between adjacent time periods support historical periodization.
- **Topic Modeling:** Early texts focus on didactic themes, while later books explore personal growth, fantasy, and emotional depth.

---

##  Machine Learning Summary

| Model               | Accuracy |
|--------------------|----------|
| Linear SVM          | 73%      |
| Logistic Regression | 67%      |
| Random Forest       | 60%      |

Linear SVM outperformed others with balanced F1 scores across all eras.

---

##  Periodization Framework

Using TF-IDF and cosine similarity (from Alsudais & Tchalian, 2016), we validated our division of the corpus into four distinct eras. Each adjacent time period had very low similarity (< 0.07), confirming stylistic shifts:

| Periods Compared           | Cosine Similarity |
|----------------------------|-------------------|
| 1700–1799 vs 1800–1899     | 0.032             |
| 1800–1899 vs 1900–1999     | 0.045             |
| 1900–1999 vs 2000+         | 0.051             |

---

##  Conclusion

This study confirms that children’s literature has undergone major stylistic and thematic changes across three centuries.
Today’s books are more accessible, emotionally engaging, and inclusive — reflecting broader societal shifts in how childhood, education, and empathy are approached.

---

