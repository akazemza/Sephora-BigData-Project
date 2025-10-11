# Sephora Big Data Analytics Project

This project analyzes customer reviews and product metadata from Sephora to identify key factors influencing product ratings and sentiment. It includes **data cleaning, exploratory data analysis (EDA), feature engineering, and predictive modeling** using both classical ML and transformer-based approaches.

---

## Repo Structure
```
Sephora-BigData-Project/
│── README.md                 # Project overview, instructions
│── data/                     # Cleaned dataset (sample only)
│── notebooks/                # Jupyter notebooks + HTML exports
│── reports/                  # Project reports (Word/PDF)
│── figures/                  # Flowchart + EDA plots
│── sephora_clean_eda.ipynb   # Main notebook
│── sephora_clean_eda.html    # Executed notebook (HTML)
│── sephora_reviews_cleaned.csv
```

---

## Data
- **Source:** Sephora product & skincare review dataset.  
- **Contents:** Product names, brands, prices, ratings, review texts, and optional user metadata (e.g., skin type).  
- **Preprocessing:** Invalid ratings removed, duplicates dropped, text normalized, numeric fields standardized.  

⚠️ Note: Only cleaned/small samples are shared here. Full raw datasets are excluded due to size/licensing.

---

## Methods
1. **Data Cleaning & Preprocessing**
   - Ratings filtered to valid range [1–5].
   - Removed duplicates, normalized text, standardized numeric fields.
2. **Exploratory Data Analysis (EDA)**
   - Rating distributions, price histograms, brand-level summaries.
   - Visualizations for skin type/tone vs. ratings.
3. **Feature Engineering**
   - Text: TF-IDF vectors, transformer embeddings (DistilBERT).
   - Metadata: price, brand, skin type, review length.
4. **Modeling**
   - Baseline: Logistic Regression, SVM.
   - Advanced: DistilBERT fine-tuned on review text.
5. **Evaluation**
   - Metrics: Accuracy, F1-score, AUC.
   - Stratified cross-validation and error analysis.

---

## Results
- Ratings skewed toward **4–5 stars**, indicating potential class imbalance.  
- Review length shows only weak correlation with rating.  
- Certain brands and skin types show systematic rating differences.  
- Transformer-based models outperform baseline ML classifiers for sentiment prediction.  

---

## How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/Sephora-BigData-Project.git
   cd Sephora-BigData-Project
   ```
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib scikit-learn transformers
   ```
3. Open the notebook:
   ```bash
   jupyter notebook notebooks/sephora_clean_eda.ipynb
   ```

---

## Deliverables
- Cleaned dataset → `data/sephora_reviews_cleaned.csv`  
- EDA figures → `figures/`  
- Final project report → `reports/`  
- Reproducible notebook → `notebooks/`  

---

## License
This project is for **academic use only**. Data is derived from Sephora public datasets and shared here for demonstration/educational purposes.
