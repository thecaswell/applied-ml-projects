# 🧠 Similarity-Based Salon Recommendation Engine

> ⚠️ This README was generated with the assistance of a Generative AI tool to document and summarize the project structure, logic, and purpose.

## 📘 Project Overview

This project implements a modular, object-oriented engine to recommend **similar salons** based on business, social, and demographic metrics. Given a query profile, the engine returns a ranked list of salons most similar to the input using **cosine similarity** on normalized feature vectors.

The architecture is designed for real-time use cases, where structured inputs are passed through a filtering and scoring logic pipeline to drive dynamic recommendations.

---

## ⚙️ Key Features

- Accepts structured input via Python dictionary
- Optional filters: salon type, minimum review rating, exclude previously visited
- Feature normalization using `MinMaxScaler`
- Similarity scoring via `cosine_similarity`
- Returns top-k most similar salons with relevant metadata

---

## 🧾 Input Data

Each salon in the dataset includes:

| Feature             | Description                                          |
|---------------------|------------------------------------------------------|
| `monthly_sales`     | Average monthly revenue (can be 0 if unvisited)      |
| `social_followers`  | Number of social media followers                     |
| `social_tags`       | Number of user-generated social tags                 |
| `check_ins`         | Location-based user visits                           |
| `avg_income`        | Average income in the salon’s surrounding area       |
| `urban_density`     | Urban population density index                       |
| `avg_review`        | Customer review rating (1.0 to 5.0 scale)            |
| `salon_type`        | Salon category label (`hair_salon`, `barber_shop`, etc.) |

---

## 🧰 Engine Class: `SalonSimilarityEngine`

### `__init__(salons_df: pd.DataFrame)`
- Loads and stores the dataset
- Defines the feature set used for similarity
- Scales numeric features to the `[0, 1]` range using `MinMaxScaler`

### `find_similar_salons(query: dict, top_k: int = 5)`
- Accepts a query dictionary with any of the feature keys
- Filters dataset based on optional fields:
  - `salon_type`: limit to a specific category of salons
  - `min_avg_review`: exclude poorly reviewed salons
  - `exclude_visited`: if `True`, exclude salons with low projected future sales
- Scales the query and the filtered dataset
- Computes cosine similarity between query and salons
- Returns the top-k most similar salons with similarity scores

---

## 🔍 Example Use Case

```python
query = {
    "salon_type": "hair_salon",
    "monthly_sales": 20000,
    "social_followers": 4500,
    "social_tags": 120,
    "check_ins": 300,
    "avg_income": 70000,
    "urban_density": 0.85,
    "avg_review": 4.5,
    "min_avg_review": 4.0,
    "exclude_visited": True
}
```

---

## 📦 Dependencies

- `pandas`
- `numpy`
- `scikit-learn`

---