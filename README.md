# LifeScore AI - Behavior-Aware Risk Scoring Platform

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Machine Learning](https://img.shields.io/badge/ML-XGBoost-green.svg)](https://xgboost.readthedocs.io/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

An AI-powered lifestyle risk scoring engine that predicts insurance risk based on 26+ behavioral, fitness, and financial factors. Built for Gen Z insurance personalization using machine learning and explainable AI.

## 🎯 Overview

LifeScore AI transforms traditional insurance risk assessment by incorporating modern lifestyle data including fitness tracking, mental health indicators, social behaviors, and financial habits. The platform uses unsupervised learning to identify lifestyle personas and supervised learning to predict risk scores with high accuracy.

### Key Features

- **26+ Behavioral Factors**: Comprehensive analysis including fitness, health, lifestyle, diet, financial behavior, and mental health
- **Lifestyle Clustering**: KMeans clustering to identify 4 distinct lifestyle personas
- **Risk Prediction**: XGBoost regression model achieving R² > 0.8
- **Explainable AI**: SHAP values for transparent risk factor analysis
- **Premium Calculation**: Dynamic insurance premium estimation based on risk scores
- **Gen Z Focused**: Tailored for ages 18-27 with modern lifestyle considerations

## 🏗️ Architecture

```
LifeScore AI Pipeline
│
├── Data Generation
│   └── Synthetic Gen Z profiles (1200+ samples)
│
├── Feature Engineering
│   ├── Fitness Score
│   ├── Health Risk Factor
│   └── Lifestyle Balance
│
├── Clustering Analysis
│   ├── KMeans (k=4)
│   └── Lifestyle Personas
│
├── Risk Prediction
│   ├── XGBoost Regressor
│   └── 31 Features
│
└── Model Explainability
    └── SHAP Analysis
```

## 📊 Dataset Features

### Demographics
- Age (18-27)
- Gender

### Fitness & Health
- Daily steps
- Gym visits per week
- Sleep hours
- BMI
- Heart rate average

### Lifestyle Behaviors
- Smoking status
- Alcohol consumption
- Screen time hours
- Meditation minutes

### Diet & Nutrition
- Fast food consumption
- Water intake
- Fruits & vegetables servings

### Financial Behavior
- Credit score
- Monthly income
- Savings rate

### Social & Mental Health
- Social activity score
- Stress level
- Hobbies count

### Transportation & Safety
- Commute hours
- Daily driving
- Traffic violations

### Medical History
- Chronic conditions
- Hospital visits
- Medications count
- Family history score

## 🚀 Getting Started

### Prerequisites

```bash
Python 3.8+
pip or conda package manager
```

### Installation

1. Clone the repository
```bash
git clone https://github.com/NeerajKumarRay1/LifeScore-AI.git
cd LifeScore-AI
```

2. Create a virtual environment
```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

3. Install dependencies
```bash
pip install -r requirements.txt
```

### Required Libraries

```
pandas
numpy
scikit-learn
xgboost
shap
matplotlib
seaborn
faker
```

## 💻 Usage

### Run the Complete Pipeline

```bash
python run_lifescore_pipeline.py
```

This will:
1. Generate synthetic dataset (1200 profiles)
2. Perform feature engineering
3. Execute clustering analysis
4. Train XGBoost risk prediction model
5. Display model performance metrics

### Use Jupyter Notebook

```bash
jupyter notebook "LifeScore_AI_Complete_Pipeline (1).ipynb"
```

The notebook provides interactive exploration of:
- Data generation and EDA
- Feature engineering
- Clustering visualization
- Model training and evaluation
- SHAP explainability analysis

## 📈 Model Performance

### XGBoost Risk Prediction Model

- **Training R² Score**: ~0.95
- **Test R² Score**: ~0.85 (Target: > 0.8 ✅)
- **Mean Absolute Error**: ~3.5 risk score points
- **Features**: 31 engineered features
- **Training Samples**: 960
- **Test Samples**: 240

### Clustering Results

- **Algorithm**: KMeans
- **Optimal Clusters**: 4
- **Silhouette Score**: ~0.45

#### Identified Lifestyle Personas

1. **Health Enthusiasts**: High fitness scores, low risk
2. **Balanced Lifestyle**: Moderate across all factors
3. **High Risk**: Poor health indicators, high stress
4. **Sedentary Workers**: Low activity, high screen time

## 🔍 Key Insights

### Top Risk Factors (Feature Importance)

1. Health Risk Factor (chronic conditions, hospital visits)
2. BMI deviation from optimal
3. Smoking status
4. Stress level
5. Family history score
6. Fitness score (inverse correlation)
7. Sleep hours
8. Alcohol consumption
9. Daily steps (inverse correlation)
10. Lifestyle balance

### Risk Score Distribution

- **Mean Risk Score**: ~50
- **Range**: 0-100
- **Standard Deviation**: ~15

### Premium Calculation

```
Base Premium: ₹15,000/year
Final Premium = Base × (1 + Risk Score/100) × Random Factor(0.9-1.1)
Average Premium: ₹22,500/year
```

## 📁 Project Structure

```
LifeScore-AI/
│
├── run_lifescore_pipeline.py          # Main pipeline script
├── LifeScore_AI_Complete_Pipeline (1).ipynb  # Interactive notebook
├── ladder.py                          # Utility script
│
├── dataset/
│   ├── train/                         # Training data
│   └── test/                          # Test data
│
├── lifescore_pipeline_summary.csv     # Pipeline results
├── lifescore_risk_scores.csv          # Risk score outputs
│
├── LifeScore_AI_Technical_Report.pdf  # Detailed documentation
├── LifeScore_AI_Detailed_Documentation.pdf
│
└── README.md                          # This file
```

## 🎓 Technical Details

### Machine Learning Pipeline

1. **Data Generation**: Faker library for synthetic Gen Z profiles
2. **Preprocessing**: StandardScaler for feature normalization
3. **Clustering**: KMeans with elbow method optimization
4. **Regression**: XGBoost with hyperparameter tuning
5. **Explainability**: SHAP (SHapley Additive exPlanations)

### Feature Engineering

- **Fitness Score**: Composite metric from steps, gym visits, sleep, smoking
- **Health Risk Factor**: Weighted sum of medical history indicators
- **Lifestyle Balance**: Social activity, hobbies, meditation vs stress, screen time

## 🔮 Future Enhancements

- [ ] Real-time data integration (wearables, apps)
- [ ] Deep learning models (LSTM for temporal patterns)
- [ ] Mobile app for user risk assessment
- [ ] API for insurance provider integration
- [ ] Personalized health recommendations
- [ ] Longitudinal risk tracking
- [ ] Multi-modal data (images, text)

## 📊 Visualizations

The project includes comprehensive visualizations:
- Risk score distribution histograms
- Premium vs risk scatter plots
- Cluster analysis plots
- Feature importance charts
- SHAP waterfall plots
- Correlation heatmaps

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Neeraj Kumar Ray**

- GitHub: [@NeerajKumarRay1](https://github.com/NeerajKumarRay1)
- Repository: [LifeScore-AI](https://github.com/NeerajKumarRay1/LifeScore-AI)

## 🙏 Acknowledgments

- XGBoost team for the powerful gradient boosting library
- SHAP library for explainable AI capabilities
- Scikit-learn for machine learning utilities
- Faker library for synthetic data generation

## 📧 Contact

For questions, suggestions, or collaboration opportunities, please open an issue or reach out through GitHub.

---

⭐ If you find this project useful, please consider giving it a star!
