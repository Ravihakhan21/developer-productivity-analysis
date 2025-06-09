#  Developer Productivity Analysis

A machine learning project that predicts whether a developer's task will succeed based on daily behavior patterns like coding time, sleep, meetings, and distractions.

---

##  Dataset
- **Source**: `ai_dev_productivity.csv`
- **Target Variable**: `task_success` (Binary: Success or Not)

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

## Evaluation (Random Forest)

- **Confusion Matrix**: `[[33, 1], [1, 65]]`
- **Classification Report**:
  - **Precision**: 0.97 (Class 0), 0.98 (Class 1)
  - **Recall**: 0.97 (Class 0), 0.98 (Class 1)
  - **F1-score**: **0.98 (Overall)**
- **Cross-Validation Accuracy**: ~0.95 (5-fold)
