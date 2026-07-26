# 🛡️ Explainable Ensemble Learning Framework for Intrusion Detection in Smart Campus Networks

An intelligent, transparent Intrusion Detection System (IDS) designed to classify campus network traffic (Normal vs. Attack) using Ensemble Machine Learning, with integrated Explainable AI (SHAP & LIME) to highlight attack indicators.

---

## 📌 Features
- **Data Preprocessing Pipeline:** Automated handling of missing values, feature scaling, and protocol encoding.
- **Ensemble ML Engine:** Stacking Random Forest, XGBoost, and LightGBM for high precision ($F1 \ge 0.95$).
- **Explainable AI (XAI):** Global feature rankings via **SHAP** and instance-level force plots via **LIME**.
- **FastAPI Microservice:** RESTful API endpoints (`/predict` and `/explain`) for low-latency inference.
- **Admin Dashboard:** Streamlit/React web portal for real-time traffic monitoring and interactive XAI plots.

---

## 📁 Repository Structure

```text
smart-campus-intrusion-detection/
├── data/               # Raw & processed datasets (UNSW-NB15 / CIC-IDS2018)
├── notebooks/          # Exploratory Data Analysis (EDA) & experimentation
├── src/                # Core modular source code
│   ├── preprocessing/  # Data cleaning & feature scaling
│   ├── models/         # Ensemble model training logic
│   └── explainability/ # SHAP & LIME calculation logic
├── app/                # FastAPI backend & Streamlit dashboard
├── saved_models/       # Serialized trained model weights (.pkl / .joblib)
├── tests/              # Unit and integration test suites
├── docs/               # PRD, architecture blueprints, & reports
├── Dockerfile          # Single-container configuration
├── docker-compose.yml  # Multi-container service setup
└── requirements.txt    # Python library dependencies
