# 🎯 Linear Regression with Gradient Descent & 5‑Fold CV

![Status](https://img.shields.io/badge/project-complete-brightgreen)
![Python 3.9](https://img.shields.io/badge/python-3.9-blue)

A hands‑on exploration of **standard linear regression** trained via gradient descent.  
Using a small dataset containing **four numeric input features (X₁ – X₄)** and a single target variable **Y**, we:

* 🔀 test **15 distinct feature‑set combinations** (all non‑empty subsets of the four inputs);  
* ♻️ apply **5‑fold cross‑validation** to each combination (75 total training runs);  
* ⏱️ employ **early stopping** to prevent over‑fitting and reduce unnecessary iterations;  
* 🏆 compare validation‑fold MSE to identify the most predictive feature set.

---

## 📊 Dataset Schema

| Column | Description |
|--------|-------------|
| X₁     | Feature 1 |
| X₂     | Feature 2 |
| X₃     | Feature 3 |
| X₄     | Feature 4 |
| **Y**  | Target value to predict |

---

## 🧮 Feature‑Set Matrix (15 Combinations)

| Size | Combinations |
|------|--------------|
| 1‑feature | {X₁}, {X₂}, {X₃}, {X₄} |
| 2‑feature | {X₁,X₂}, {X₁,X₃}, {X₁,X₄}, {X₂,X₃}, {X₂,X₄}, {X₃,X₄} |
| 3‑feature | {X₁,X₂,X₃}, {X₁,X₂,X₄}, {X₁,X₃,X₄}, {X₂,X₃,X₄} |
| 4‑feature | {X₁,X₂,X₃,X₄} |

---

## ⚙️ Methodology

1. **Gradient Descent**  
   * Implemented manually in pure Python 3.9 (no high‑level ML libraries).  
   * Learning‑rate and max‑epoch hyper‑parameters exposed for experimentation.  
2. **Early Stopping**  
   * Monitors validation‑fold loss; halts when no improvement after *N* epochs.  
3. **5‑Fold Cross‑Validation**  
   * Data shuffled once with a fixed random seed for reproducibility.  
   * Each fold provides train/validation splits; average MSE reported.  
4. **Model Selection**  
   * Best feature sets compared by mean validation MSE across folds.  

---

## 🔑 Data Requirements

This notebook expects a CSV named `data1.csv` in the repository root containing the columns shown in the **Dataset Schema** above.

> **Note:** The dataset was provided by the course instructor and is **not redistributed** here.  
> If you have legitimate access, place your copy of `data1.csv` beside the notebook before running.

---

## 📁 Files

- `lin_reg_gd.ipynb` — Notebook that trains a gradient‑descent linear‑regression model (loads `data1.csv` locally)  
- `README.md` — You are here

---

### In Summary:
A compact, reproducible showcase of gradient‑descent linear regression with exhaustive feature‑set testing, 5‑fold CV, and early stopping—ready for reviewers to explore (once they supply the data).

## Author

*Prepared by Barrett James McDonald | PhD Student | University of South Florida*

---

If you have any questions or feedback, feel free to contact me or open an issue. 💬
