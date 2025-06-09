#  Developer Productivity Analysis

A machine learning project that predicts whether a developer's task will succeed based on daily behavior patterns like coding time, sleep, meetings, and distractions.

---

##  Dataset
- **Source**: [Kaggle – AI Developer Productivity Dataset](https://www.kaggle.com/datasets/atharvasoundankar/ai-developer-productivity-dataset)
- **Target Variable**: `task_success` (Binary: Success or Not)

⚠ Dataset is **not included** in this repository due to redistribution restrictions.  
You can download it directly from the Kaggle link above and place the file `ai_dev_productivity.csv` in the project folder to run the notebooks.

###  Features Used:
- `coding_hours`
- `sleep_hours`
- `meeting_hours`
- `distractions`

 **Dropped Features**:
- `coffee_intake_mg`
- `cognitive_load`  
*Dropped due to multicollinearity to improve model generalization.*

---

##  Models Tested

| Model                | Accuracy | Notes                                      |
|---------------------|----------|--------------------------------------------|
| Logistic Regression | 0.86     | High precision for successful tasks        |
| Decision Tree       | 0.96     | Excellent performance, slight overfitting  |
| Random Forest       | **0.98** | Best overall performance                   |

---

##  Evaluation (Random Forest)

- **Confusion Matrix**: `[[33, 1], [1, 65]]`
- **Classification Report**:
  - **Precision**: 0.97 (Class 0), 0.98 (Class 1)
  - **Recall**: 0.97 (Class 0), 0.98 (Class 1)
  - **F1-score**: **0.98 (Overall)**
- **Cross-Validation Accuracy**: ~0.95 (5-fold)

---

##  Feature Importance (Random Forest)

1. `coding_hours` – Most impactful  
2. `sleep_hours`  
3. `meeting_hours`  

---

##  Final Insight

The **Random Forest model** achieved the highest performance with 98% accuracy, showing that **productive coding hours and sufficient sleep** are key predictors of task success.

> **"More sleep and deep work, less chaos — a recipe for coding success."**

---

## 🛠️Tools Used
- Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)  
-  Google Colab

---

## Contact

**Raviha Khan**  
🔗 [LinkedIn](https://www.linkedin.com/in/raviha-khan-ab17b424a)  
🐙 [GitHub](https://github.com/Ravihakhan21)  
📧 ravihakhan53@gmail.com  
📍 Karachi, Pakistan  
📱 0332-5214319
