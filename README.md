# Identifying-Quora-Question-Pairs
In this project, I use sentence embeddings to identify question pairs. I use logistc regression as a baseline model, then use random forest and XGBoost. 


# Logistic Regression Results (Baseline)

| Model                                                 | True Positive | True Negative  | False Positive | False Negative | Accuracy | Precision | Recall | F1-Score | AOC AUC | Log Loss |
|-------------------------------------------------------|---------------|----------------|----------------|----------------|----------|-----------|--------|----------|---------|---------|
| Logistic Regression (Original Embeddings, Unbalanced) | 1916          | **5391**       | 1711           | **982**        |**0.7307**|**0.6611**| 0.5283 | 0.5873   | 0.7732  | **0.5417** |
| Logistic Regression (Original Embeddings, Balanced)   | **2531**      | 4526           | **1096**       | 1847           | 0.7057   | 0.5781    |**0.6978**|**0.6324**|**0.7735**| 0.5698 |
| Logistic Regression (Cleaned Embeddings, Unbalanced)  | 1636          | 5375           | 1991           | 998            | 0.7011   | 0.6211    | 0.4511 | 0.5226   | 0.7339  | 0.5739 |
| Logistic Regression (Cleaned Embeddings, Balanced)    | 2447          | 4252           | 1180           | 2121           | 0.6699   | 0.5357    | 0.6747 | 0.5972   | 0.7328  | 0.6065 |

# Random Forest Results

| Model                                           | True Positive | True Negative  | False Positive | False Negative | Accuracy | Precision | Recall | F1-Score | AOC AUC | Log Loss |
|-------------------------------------------------|---------------|----------------|----------------|----------------|----------|-----------|--------|----------|---------|----------|
| Random Forest (Original Embeddings, Unbalanced) | **1777**      | 6042           | **1850**      | 331            |**0.7819**  | 0.8430    |**0.4899**|**0.6197**| 0.8500  | 0.4959   |
| Random Forest (Original Embeddings, Balanced)   | 1712          | **6100**       | 1915          | **273**        | 0.7812   |**0.8625** | 0.4720 | 0.6101   |**0.8546**|**0.4907**|
| Random Forest (Cleaned Embeddings, Unbalanced)  | 1545          | 5987           | 2082          | 386            | 0.7532    | 0.8001    | 0.4260 | 0.5560   | 0.8109  | 0.5295   |
| Random Forest (Cleaned Embeddings, Balanced)    | 1480          | 6048           | 2147          | 325            | 0.7528    | 0.8199    | 0.4081 | 0.5449   | 0.8193  | 0.5236   |

# XGBoost Results

| Model                         | True Positive | True Negative  | False Positive | False Negative | Accuracy | Precision | Recall | F1-Score | AOC AUC | Log Loss |
|-------------------------------|---------------|----------------|----------------|----------------|----------|-----------|--------|----------|---------|----------|
| XGBoost (Original Embeddings) |**2539**       |**5533**        |**1088**        |**840**         |**0.8072**|**0.7514** | **0.7000**|**0.7248**|**0.8801**|**0.4149**|
| XGBoost (Cleaned Embeddings)  | 2141          | 5376           | 1486           | 997            | 0.7517   | 0.6823    | 0.5903 | 0.6330   | 0.8194  | 0.4942   |
