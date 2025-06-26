# SONAR-Rock-vs-Mine-Classification
This project applies machine learning techniques to classify objects detected by SONAR as either rocks or mines based on reflected signal data. The dataset contains 60 sonar signal features per instance, and the model learns to distinguish between natural underwater formations and potential threats like mines.
# 🧭 SONAR Rock vs Mine Prediction using Machine Learning

This project builds a binary classification model using the **SONAR dataset** to distinguish between **underwater rocks** and **mines** based on sonar signal returns. This system is vital for underwater navigation, marine defense, and autonomous underwater vehicles (AUVs).

---

## 📈 Project Overview

- This is a **supervised machine learning** project focused on **binary classification**.
- The model used: **Logistic Regression**
- Dataset Source: Included locally as `Copy of sonar data.csv` in the repository
- Evaluation Metric: **Accuracy Score**
- Target Labels:  
  - `R` = Rock  
  - `M` = Mine

---

## 📊 Dataset Description

The dataset consists of **208 instances** and **61 columns**:

| Feature Range | Description                       |
|---------------|-----------------------------------|
| 0 - 59        | Sonar signal strength features     |
| 60            | Target label (R = Rock, M = Mine) |

---

## 🔧 Tech Stack & Libraries Used

- **Python**
- **NumPy**, **Pandas** – Data manipulation
- **Scikit-learn** – Model training, testing, and evaluation

---

## 🧠 Model Training

- Features and labels were separated from the dataset.
- Data was split into:
  - **Training set**: 90%
  - **Testing set**: 10%
- Model Used: `LogisticRegression()`

### 📋 Accuracy Results

| Dataset        | Accuracy     |
|----------------|--------------|
| Training Set   | ~83.42%      |
| Testing Set    | ~76.19%      |

---

## 🔍 Prediction Example

After training, the model can classify new sonar data:

```python
input_data = (0.0453, 0.0523, 0.0843, ..., 0.0044)  # sample sonar input
prediction = model.predict([input_data])
# Output: ['R'] → The object is a Rock
```
## 🚀 How to Run This Project

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/sonar-rock-vs-mine-prediction.git 
   cd sonar-rock-vs-mine-prediction
   ```
2. 2. Run the Jupyter Notebook:
   ````bash
   jupyter notebook

## 📙 Future Improvements

- 🔧 Try different classification models like **Random Forest**, **SVM**, or even deep learning models
- 🌐 Deploy the model using [Flask](https://flask.palletsprojects.com/ ) or [Streamlit](https://streamlit.io/ ) for a live web demo
- 📊 Visualize performance metrics using a **confusion matrix** and **ROC curve**
- ⚖️ Add **K-Fold Cross-Validation** for more robust model evaluation

## 🙌 Acknowledgements

- [UCI ML Repository - Sonar Dataset](https://archive.ics.uci.edu/ml/datasets/Connectionist+Bench+ (Sonar,+Mines+vs.+Rocks))
