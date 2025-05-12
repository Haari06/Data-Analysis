Loan Classification Model – README
📄 Project Overview
This project involves building a classification model to predict the loan status (i.e., whether a loan is paid off or in collection) using a dataset containing details about previous loans. The goal is to evaluate and compare the performance of four machine learning algorithms on this task.

📂 Dataset Description
The dataset Loan_train.csv contains 346 records with the following features:

Field	Description
Loan_status	Target variable: whether the loan is "PAIDOFF" or "COLLECTION"
Principal	Loan amount principal
Terms	Payment terms: weekly (7 days), biweekly, or monthly
Effective_date	Start date of loan
Due_date	Loan payoff due date
Age	Age of the applicant
Education	Educational background of the applicant
Gender	Applicant’s gender

🧹 Preprocessing Steps
To ensure optimal model performance, the following preprocessing techniques were applied:

Converted categorical variables (Education, Gender, Terms) to numerical values using OneHotEncoding and LabelEncoding

Converted Effective_date and Due_date to datetime and extracted relevant features (like day of week)

Normalized numerical features (Principal, Age) using StandardScaler

Handled class imbalance using resampling, if needed

🧠 Algorithms Used
The following classification models were implemented using scikit-learn:

Algorithm	Description
K-Nearest Neighbors (KNN)	Uses proximity of feature space to classify loan status
Decision Tree	Splits data based on most significant features using tree structures
Support Vector Machine (SVM)	Finds a decision boundary that best separates the two loan classes
Logistic Regression	Estimates probability of loan repayment using logistic function

📊 Model Evaluation Metrics
Each model was evaluated using:

Jaccard Index – Similarity between predicted and actual labels

F1-score – Harmonic mean of precision and recall

LogLoss – Logarithmic loss metric used for probabilistic classifiers (Logistic Regression only)

Algorithm	Jaccard	F1-score	LogLoss
KNN	0.67	0.48	NA
Decision Tree	0.78	0.60	NA
SVM	0.72	0.42	NA
Logistic Regression	0.74	0.43	0.55

🛠️ Libraries and Tools Used
Python

scikit-learn

NumPy

Pandas

Matplotlib / Seaborn (for visualization)

📁 Folder Structure
bash
Copy code
Loan-Classification-Project/
│
├── Loan_train.csv
├── Loan_test.csv
├── loan_classification.ipynb       # Jupyter Notebook with model training and evaluation
├── README.md                       # Project overview and documentation
🚀 Conclusion
Among all the models tested, the Decision Tree classifier yielded the highest performance in terms of Jaccard and F1-score. Future improvements could include hyperparameter tuning, handling class imbalance, or trying ensemble methods like Random Forests or Gradient Boosting.

