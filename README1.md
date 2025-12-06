# Amazon Product Rating Prediction — Deep Learning Model

This project focuses on developing a Deep Learning model to predict product ratings using the Amazon dataset. The model is trained for multiple epochs to minimize loss and maximize prediction accuracy. Performance is evaluated using standard regression error metrics including MAE, MSE, RMSE and R² score.

This repository demonstrates the complete machine learning pipeline including preprocessing, model creation, training, evaluation and prediction.

---

## Project Overview

| Task Component                         | Status    |
| -------------------------------------- | --------- |
| Data Cleaning & Preprocessing          | Completed |
| Train–Test Split                       | Completed |
| Deep Learning Model (TensorFlow/Keras) | Completed |
| Epoch-based Training                   | Completed |
| Error Metrics Calculation              | Completed |
| Saving Trained Model                   | Completed |
| Predictions CSV Export                 | Completed |

---

## Dataset Description

The model is trained on the Amazon product dataset. The dataset consists of review-based features that influence product ratings.

| Feature             | Description                   |
| ------------------- | ----------------------------- |
| product_id          | Unique ID of the product      |
| product_name        | Name of the product           |
| category            | Product category              |
| discounted_price    | Selling price                 |
| actual_price        | Original price                |
| discount_percentage | Discount offered              |
| rating              | Target column to be predicted |
| rating_count        | Number of ratings received    |
| about_product       | Text description              |
| user_id             | Unique ID of reviewer         |
| user_name           | Name of the reviewer          |
| review_id           | Review identity               |
| review_title        | Title of the review           |
| review_content      | Full review text              |

Note: The **rating** column is the target label for prediction.

---

## Deep Learning Model Architecture

The rating prediction model is built using TensorFlow/Keras Sequential API with the following structure:

```
Input Layer
Dense — 64 units, ReLU
Dense — 32 units, ReLU
Dropout — 0.2
Dense — 16 units, ReLU
Output Layer — 1 unit (Regression)
```

Additional configuration:

| Component          | Details                                |
| ------------------ | -------------------------------------- |
| Loss Function      | Mean Squared Error (MSE)               |
| Optimizer          | Adam                                   |
| Evaluation Metrics | MAE, MSE, RMSE, R²                     |
| Epochs             | Trained for N epochs until convergence |

---

## Evaluation Metrics

| Metric   | Meaning                                            |
| -------- | -------------------------------------------------- |
| MAE      | Measures average magnitude of errors               |
| MSE      | Squared error magnitude (penalizes large errors)   |
| RMSE     | Square root of MSE for easier interpretation       |
| R² Score | Indicates accuracy (0 to 1, closer to 1 is better) |

The model achieving the best results is automatically saved.

---

## Output Files in Repository

| File Name                         | Description                             |
| --------------------------------- | --------------------------------------- |
| `best_model.keras`                | Best trained Deep Learning model        |
| `predictions.csv`                 | Contains actual vs predicted ratings    |
| `training_results.txt` (optional) | Logs of loss and metrics for each epoch |

---

## How to Run

### Step 1: Install Dependencies
```bash
pip install pandas numpy scikit-learn tensorflow
```

### Step 2: Train the Model
```bash
python model.py
```

### Step 3: Run Predictions Using Saved Model
```bash
python predict.py
```

---

## Conclusion

This project successfully builds and trains a deep learning regression model for predicting Amazon product ratings. It demonstrates:

* Effective preprocessing and feature engineering
* Multi-epoch training to minimize loss
* Model accuracy evaluation using key regression metrics
* Exporting predictions and saving the trained model

The model can be extended for deployment as an API or Web App for real-time prediction.

---

## Future Scope

* Integration of sentiment analysis from review text
* Hyperparameter tuning for better accuracy
* Use of Transformer/NLP embeddings for review content
* Deployment using Flask, Streamlit or cloud platforms

---

### Author

Academic project on Machine Learning with Deep Learning regression for rating prediction.
