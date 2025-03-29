
# 🇺🇦 Ukraine War Tweets: Sentiment Analysis + Topic Discovery

This project leverages deep learning and natural language processing techniques to analyze global sentiment and discourse around the Russia-Ukraine war on Twitter. Using a Bidirectional LSTM model for **sentiment classification** and Latent Dirichlet Allocation (LDA) for **topic modeling**, we explore how public emotions and topics of discussion evolved during the early months of the conflict.

---

## 👨‍💻 Authors

- Yifei Song  
- Keying Gong  
- Zhirui Li  
- Hanjun Wei  

Course: Brown University, CS2470 — Deep Learning  
Date: May 13, 2022

---

## 📌 Project Objectives

- **Understand emotional reactions** of English-speaking Twitter users to the Russia-Ukraine war.
- **Track sentiment evolution** over time.
- **Discover hidden discussion topics** through unsupervised modeling.
- **Link topics to emotions** for richer psychological insight.

---

## 🧹 Preprocessing Pipeline

1. **Remove special characters & retweets**
2. **Lowercase & remove short words**
3. **Stopword removal**
4. **Lemmatization**

Example:
```
Original Tweet:
RT @NYTimes: #BREAKING SUNDAY: RAW VIDEO OF #Russian Column Destroyed By #Ukraine Forces Near #Kyiv

Preprocessed:
break sunday raw video russian column destroyed ukraine forces near kyiv
```

---

## 🔍 Sentiment Analysis

### Model: **Bidirectional LSTM**

- **Embedding**: GloVe word vectors
- **Architecture**: BiLSTM → Dense (Sigmoid)
- **Output**: 11 multi-label sentiments (anger, joy, disgust, fear, etc.)
- **Decision threshold**: 0.37 (based on F1-micro score)
- **Performance**: F1-score ≈ 0.66

### Insights:

- Most common sentiments: **disgust**, **fear**, **joy**
- Negative sentiments (e.g., anger, disgust) decrease over time
- Positive sentiment (e.g., joy) shows an increasing trend

---

## 🧠 Topic Discovery

### Model: **Latent Dirichlet Allocation (LDA)**

- Unsupervised clustering of tweet content into **12 latent topics**
- Topics manually interpreted using keyword clouds

#### Example Clusters:
- **Pro-Ukraine Sentiment**: "life", "good", "protect", "freedom", "hope", "stand", "love"
- **Anti-War/Russia Sentiment**: "putin", "war_crimes", "genocide", "stopwar"

---

## 📈 Key Results

- Over **50%** of tweets exhibit negative sentiments
- Sentiment trends **evolve gradually** over time
- LDA clusters provide context-specific sentiment interpretations
- Visualization of sentiment trends and topic clusters enabled richer storytelling

---

## 🧩 Challenges

- Difficulties in sourcing **multi-label sentiment data**
- Selecting the optimal **threshold** for prediction confidence
- Long training times for LDA model on large datasets
- Need for **more diverse sentiment labels** beyond the original 11

---

## 📚 References

1. Mohammad, Saif, et al. "Semeval-2018 Task 1: Affect in Tweets." (2018)  
2. BWANDOWANDO. "Ukraine Conflict Twitter Dataset." Kaggle, 2022  
3. Pennington, Socher, & Manning. "GloVe: Global Vectors for Word Representation." EMNLP, 2014  
4. Blei, Ng, Jordan. "Latent Dirichlet Allocation." JMLR, 2003  
5. Newman, David, et al. "Automatic Evaluation of Topic Coherence." NAACL, 2010

---

## 🔮 Future Directions

- Add more **granular sentiment labels** using human-annotated datasets
- Introduce **attention mechanisms** to improve BiLSTM interpretability
- Enhance topic-sentiment linkage using **hybrid models**
- Deploy as a live tracker for **real-time sentiment monitoring**

---

## 📂 Files Included

- `Final Report.docx`: Full report with methodology, results, and discussion
- `Poster.jpg`: Visual project summary
- `Presentation.pptx`: Project presentation slides
- `notebooks/`: (Optional) Jupyter notebooks used for modeling
