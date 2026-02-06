# Performance Metrics for Classification

This notebook provides an interactive introduction to **performance metrics used in evaluating classification models**. It is adapted from Aurélien Géron's Chapter 3 notebook under the Apache v2 License.

## Purpose

The focus is on **evaluating classifiers**, not on training them. Students will explore key metrics used to assess classification performance, such as:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- ROC Curve and AUC

## Learning Format

This notebook is designed for **active learning** in a classroom setting. Students are encouraged to:

- Run code cells during instruction
- Respond to questions marked "_To the student_" in new cells
- Take notes and annotate the notebook
- Commit and push their personalized version to their own repository

## What is Classification?

Classification is a supervised learning task where the goal is to assign input data to one of several predefined categories. A **classifier** is an algorithm or function that performs this mapping from input features to class labels.

Examples include:
- Email spam detection
- Medical diagnosis
- Image recognition

For more background, see the Wikipedia article on classification and classification algorithms.

### 🌝T.Liu Note:Takeaways

### 1. The Core Metrics
* **Precision (Quality)**: When the model predicts "Positive," how often is it right? (Goal: Minimize False Positives).
* **Recall (Quantity)**: Of all actual positive cases, how many did the model find? (Goal: Minimize False Negatives).
* **F1 Score**: The **harmonic mean** of Precision and Recall. It provides a single balanced score. It is stricter than a simple average because it punishes extreme values.

### 2. Precision/Recall Trade-off
* **The Threshold**: The "passing grade" for a prediction.
    * **Higher Threshold**: Precision ↑, Recall ↓. The model is "Strict."
    * **Lower Threshold**: Precision ↓, Recall ↑. The model is "Generous."
* **Decision Rule**:
    * Optimize **Recall** if "Missing it" is dangerous (e.g., Cancer detection).
    * Optimize **Precision** if "Being wrong" is costly (e.g., Financial investment).

### 3. ROC Curve vs. Precision-Recall (PR) Curve
* **ROC Curve**: Plots True Positive Rate vs. False Positive Rate. Best for **balanced** datasets.
* **PR Curve**: Best for **imbalanced** datasets (where the positive class is rare, like MNIST '5's).
* **Why?**: ROC can look "too optimistic" on imbalanced data. The PR curve is a more "honest" measure of how well the model identifies the rare target class.

