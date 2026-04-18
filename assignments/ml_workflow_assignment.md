# ML Workflow Assignment: Repeat Purchase Prediction

## Task 1: Label and Data Leakage

* **Label:** `repeat_purchase_flag`
    * **Justification:** This column represents the ground truth or the target outcome we want the model to predict (whether a repeat purchase occurred).
* **Data Leakage Feature:** `discount_used_on_repeat_order`
    * **Justification:** This feature provides information about the repeat purchase itself; since the discount is only applied *during* that future transaction, including it would give the model "future" information it wouldn't have in a real-world scenario.

---

## Task 2: Critical ML Workflow Steps

Before training a complex gradient boosting model, the following two steps are essential to ensure model reliability:

### 1. Exploratory Data Analysis (EDA)
**Why it matters:** EDA allows you to understand the distribution of your data, detect outliers, and identify correlations between features. Without this step, you might train a model on biased data or miss simple insights that could significantly improve performance without needing a complex algorithm.

### 2. Data Splitting (Train/Test Split)
**Why it matters:** You must separate your data into training and testing sets before looking at the model's results. This ensures that you can evaluate the model's ability to generalize to new, unseen data, preventing **overfitting** where a model simply "memorizes" the training dataset.

