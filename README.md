# MEAM Emotion Clustering & Modeling

This repository contains the code and data used to explore how **age** and **thematic content of memories** (derived from clustering) relate to **mixed emotionality** in autobiographical music-evoked memories.

---

## 🔍 Research Aim

The analysis investigates whether **age** predicts the **degree of emotional complexity (mixed emotions)** recalled in MEAMs, and whether this relationship is **moderated by thematic clusters** derived from SBERT-embedded memory descriptions.

---

## 📁 File Structure

```
├── data/
│   ├── MEAMdata_complete.xlsx               # Full dataset with metadata, GoEmotion labels, age info
│   └── SBERT/SBERT-L6-v2_embed.csv         # SBERT embeddings of memory descriptions
│
├── output/
│   ├── MEAM_fuzzy_clustered.csv            # Fuzzy cluster labels and memberships from UMAP features
│   └── OLS_Regression_Results.xlsx         # Results of the regression model (Age × Theme → Mixed Emotions)
│
├── notebooks/
│   ├── Analysis2.ipynb                     # UMAP + Fuzzy C-Means clustering
│   └── Model.ipynb                         # Regression model (OLS) on age, emotion count, and cluster
│
├── requirements.txt                        # Python package requirements
└── README.md                               # This file
```

---

## 📊 Method Summary

- **UMAP** used to reduce SBERT embeddings to 2D space.
- **Fuzzy C-Means clustering** applied to UMAP outputs (n=2–4 clusters).
- **Mixed emotions** calculated as the count of GoEmotion-derived binary labels per memory.
- **OLS regression** tested whether Age × Cluster membership predicts mixed emotion scores.

---

## 📈 Key Output

You can view the model results in:  
📄 `output/OLS_Regression_Results.xlsx`

---

## 🧪 How to Run

To recreate the analysis:

1. Clone this repo
2. Create a virtual environment
3. Run:  
   ```bash
   pip install -r requirements.txt
   ```
4. Open the notebooks in Jupyter and run cell-by-cell

---

## 🧠 Next Steps

- Replace GoEmotion-derived mixed emotion scores with **self-reported** ones
- Integrate **memory age** as a covariate
- Optimize the number of fuzzy clusters for better thematic sensitivity

---

## 📬 Contact

Feel free to leave comments or suggestions. Feedback is welcome!
