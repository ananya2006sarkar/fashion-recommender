# Fashion Product Recommender — Myntra Dataset

A content-based filtering recommendation system built on real Myntra fashion data. 
Users input their preferences (gender, category, colour, usage) and the system 
returns the most relevant products using a scoring algorithm.

## Dataset
[Fashion Product Images (Small)](https://www.kaggle.com/datasets/paramaggarwal/fashion-product-images-small) 
by paramaggarwal — 44,000+ products, cleaned to 21,367 apparel records.

## Tech Stack
- Python, pandas, NumPy
- scikit-learn (LabelEncoder, cosine similarity)
- IPython.display (in-notebook UI)
- Google Colab / Jupyter Notebook

## How It Works
1. Load and clean the Myntra dataset (filter to Apparel only, drop nulls)
2. Encode categorical features (gender, subCategory, colour, usage) using LabelEncoder
3. Hard-filter by gender + subCategory for precision
4. Score remaining products: +2 for colour match, +1 for usage match
5. Return top N products sorted by score

## Why Content-Based Filtering?
Content-based filtering recommends items similar to what the user specifies,
based purely on item attributes — no user history needed. Same technique used
by Myntra, Netflix, and Spotify at scale.
