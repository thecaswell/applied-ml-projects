# 🧠 Applied ML Projects

A collection of machine learning projects exploring various domains, including forecasting, classification, recommendation systems, and language modeling. Each project is actively under development and serves as part of a broader portfolio demonstrating applied ML capabilities.

---

## 📁 Project Structure

```
applied-ml-projects/
│
├── archive/                          # Deprecated or earlier versions of projects
│   ├── 26_week_forecast.ipynb
│   └── forecasting_sales.ipynb
│
├── classification/                  # Classification models using structured data
│   ├── data/
│   │   └── pokemon_data.csv
│   └── src/
│       └── 01_logistic_regression.ipynb
│
├── forecasting/                     # Time series forecasting projects
│   ├── data/
│   │   └── takehome_data.csv
│   └── src/
│       ├── 01_linear_regression.ipynb
│       └── 02_ridge_and_lass_regression.ipynb
│
├── llm/                             # Experiments with large language models
│   └── (WIP)
│
├── python_practice/                 # General Python and OOP practice notebooks
│   └── oop.ipynb
│
├── recommendation_engine/          # Recommender systems for synthetic beauty datasets
│   ├── data/
│   │   ├── synthetic_product_data.csv
│   │   └── synthetic_salon_dataset.csv
│   └── src/
│       ├── 01_salon_recommendation_engine.ipynb
│       └── 02_beauty_recommender_two_stage.ipynb
│
├── README.md
├── poetry.lock
├── pyproject.toml
└── .gitignore
```

---

## ✅ Project Categories

### 🔍 Classification
- Logistic Regression on Pokémon dataset.

### 📈 Forecasting
- Linear, Ridge, and Lasso regression on weekly sales data.

### 🧬 Recommendation Engines
- Collaborative filtering and two-tower recommender systems on synthetic beauty datasets.

### 💬 LLM Experiments
- Placeholder for future work on local LLM-based applications.

### 🐍 Python Practice
- Notebook for object-oriented programming (OOP) review and exploration.

---

## 🛠️ Setup

Install dependencies using [Poetry](https://python-poetry.org/):

```bash
poetry install
```

Launch Jupyter:

```bash
poetry run jupyter notebook
```

---

## 📌 Notes

- All notebooks are works in progress and subject to change.
- Datasets are synthetic or anonymized.
- Some projects are exploratory or prototypes for future blog posts and presentations.

---

## 📅 Roadmap

- [ ] Add EDA modules across all projects
- [ ] Consolidate shared preprocessing scripts
- [ ] Evaluate model performance using custom metrics
- [ ] Add testing and automation for production-ready models
