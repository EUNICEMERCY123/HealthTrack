# HealthTrack — AI-Assisted Tele - Medicine Support System for Rural India

HealthTrack is a simple web-based health application featuring a symptom checker, a stroke risk screener, and a personal health tracker. Inspired by Smart India Hackathon problem statement SIH1325, **AI-Assisted Tele-medicine Support System for Rural India**, the project demonstrates how data science and machine learning can support preliminary health screening.

**Live Application:** https://eunicemercy123.github.io/HealthTrack/

## Features

- **Symptom Checker:** Suggests possible diseases based on user-selected symptoms.
- **Stroke Risk Screener:** Generates a screening score using six inputs: age, hypertension, heart disease, average glucose level, BMI, and smoking status.
- **Personal Health Tracker:** Saves health readings and screening records for reviewing previous results.
- **Dashboard:** Displays health information and historical records.
- **Local Data Storage:** Stores records in the user's browser.
- **Safety Alerts:** Displays warnings for selected red-flag symptoms.

## Machine Learning

The project uses two publicly available Kaggle datasets:

| Dataset | Purpose |
|---|---|
| Disease Symptom Prediction | Multi-class disease classification based on symptoms |
| Stroke Prediction Dataset | Binary stroke risk screening |

Three classification algorithms were compared:

- Logistic Regression
- K-Nearest Neighbours (KNN)
- Decision Tree

The models were evaluated using five-fold cross-validation and appropriate classification metrics.

### Reported Results

| Task | Selected Model | Result |
|---|---|---|
| Symptom prediction | Logistic Regression | 1.00 test accuracy |
| Stroke screening | Logistic Regression | 0.80 recall |
| Stroke screening | Logistic Regression | 0.841 AUC |

**Note:** The symptom prediction accuracy may be overly optimistic because the dataset contains near-duplicate records. The stroke model also produces false positives. Neither model has been clinically validated.

## Technologies Used

- **Python:** Data processing and model development
- **pandas and NumPy:** Data manipulation
- **scikit-learn:** Machine learning and evaluation
- **SciPy:** Statistical testing
- **Matplotlib:** Data visualisation
- **Google Colab:** Model development and experimentation
- **HTML, CSS and JavaScript:** Web application development
- **GitHub Pages:** Application hosting
- **Playwright:** Automated browser testing

## Project Workflow

1. **Data Collection:** Load the two Kaggle datasets into Google Colab.
2. **Data Preparation:** Clean the data, encode features, and perform exploratory data analysis.
3. **Model Building:** Train Logistic Regression, KNN, and Decision Tree classifiers.
4. **Model Evaluation:** Compare model performance using cross-validation and classification metrics.
5. **Deployment:** Export the selected model parameters and integrate them into the browser-based application.

## Project Links

- **Live Application:** [HealthTrack](https://eunicemercy123.github.io/HealthTrack/)
- **Notebook:** `HealthTrack.ipynb` — open in Google Colab.
- **Disease Dataset:** [Disease Symptom Prediction on Kaggle](https://www.kaggle.com/datasets/itachi9604/disease-symptom-description-dataset)
- **Stroke Dataset:** [Stroke Prediction Dataset on Kaggle](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)

## Privacy

HealthTrack stores saved health records in the browser's local storage. These records are not intended to be transmitted to a project server. Records may be lost if browser data is cleared and may be accessible to other people using the same browser profile.

## Project Information

- **Project Name:** HealthTrack
- **Domain:** Data Science and Healthcare Analytics
- **Course:** Data Science Ecosystem
- **Course Code:** 23CS2024
- **Institution:** Karunya Institute of Technology and Sciences

---

Developed as an academic data science project inspired by SIH1325.
