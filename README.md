# UEFA Champions League (UCL) Winner Prediction System

This project uses Machine Learning to predict UEFA Champions League (UCL) winners based on group stage performance statistics.

## 📋 Project Overview

The UEFA Champions League Winner Prediction System leverages historical group stage data and advanced machine learning algorithms to forecast potential tournament winners. By analyzing team performance metrics, this system provides data-driven predictions for one of football's most prestigious competitions.

## 🗂️ Project Structure

```
UEFA-Champions-League-UCL-Winner-Prediction-System/
│
├── UCL_Winner_Prediction/
│   ├── data/              # Dataset files and data processing scripts
│   ├── models/            # Trained machine learning models
│   ├── notebooks/         # Jupyter notebooks for analysis and experimentation
│   ├── predictions/       # Prediction outputs and results
│   └── visualizations/    # Charts, graphs, and visual analytics
│
└── README.md             # Project documentation
```

## 🎯 Features

- **Data Analysis**: Comprehensive analysis of UEFA Champions League group stage statistics
- **Machine Learning Models**: Implementation of various ML algorithms for prediction
- **Performance Metrics**: Evaluation of model accuracy and reliability
- **Visualizations**: Interactive charts and graphs for data insights
- **Prediction System**: Automated winner prediction based on group stage performance

## 🚀 Getting Started

### Prerequisites

- Python 3.7+
- Jupyter Notebook
- Required Python libraries (pandas, numpy, scikit-learn, matplotlib, seaborn, etc.)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/Nazmul1005/UEFA-Champions-League-UCL-Winner-Prediction-System.git
cd UEFA-Champions-League-UCL-Winner-Prediction-System
```

2. Install required dependencies:
```bash
pip install ( necessary libraries)
```

3. Navigate to the notebooks directory:
```bash
cd UCL_Winner_Prediction/notebooks
```

4. Launch Jupyter Notebook:
```bash
jupyter notebook
```

## 📊 Dataset

The project uses UEFA Champions League group stage statistics including:
- Team performance metrics
- Match results
- Goals scored and conceded
- Points accumulated
- Historical tournament outcomes

## 🤖 Machine Learning Approach

The prediction system employs various machine learning techniques:
- Data preprocessing and feature engineering
- Model training and validation
- Performance evaluation
- Prediction generation

## 📈 Results

Prediction results and model performance metrics can be found in the `predictions/` directory, with visualizations available in the `visualizations/` folder.

## 🛠️ Technologies Used

- **Python**: Core programming language
- **Jupyter Notebook**: Interactive development environment
- **Pandas & NumPy**: Data manipulation and analysis
- **Scikit-learn**: Machine learning algorithms
- **Matplotlib & Seaborn**: Data visualization

### Ensemble Learning Approach

```
┌─────────────────────────────────────────────────────┐
│              INPUT: Group Stage Stats               │
│  (Wins, Draws, Losses, Goals, Points, etc.)        │
└──────────────────┬──────────────────────────────────┘
                   │
                   ▼
┌─────────────────────────────────────────────────────┐
│            FEATURE ENGINEERING (22 features)        │
│  - Win Ratio          - Goal Efficiency             │
│  - Loss Ratio         - Defensive Strength          │
│  - Goals Per Match    - Dominance Score             │
│  - Points Per Match   - Clean Sheet Potential       │
└──────────────────┬──────────────────────────────────┘
                   │
                   ▼
┌─────────────────────────────────────────────────────┐
│               ENSEMBLE MODELS                       │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐         │
│  │ Random   │  │   KNN    │  │ XGBoost  │         │
│  │ Forest   │  │  Model   │  │  Model   │         │
│  └────┬─────┘  └────┬─────┘  └────┬─────┘         │
│       │             │             │                 │
│       └─────────────┴─────────────┘                │
│                     │                               │
│                     ▼                               │
│          ┌──────────────────────┐                  │
│          │  WEIGHTED ENSEMBLE   │                  │
│          │   (Softmax Applied)  │                  │
│          └──────────────────────┘                  │
└──────────────────┬──────────────────────────────────┘
                   │
                   ▼
┌─────────────────────────────────────────────────────┐
│              OUTPUT: Win Probabilities              │
│         (Top 16 Teams Ranked by Likelihood)         │
└─────────────────────────────────────────────────────┘
```


### Test Set Validation (2021-2024)

| Season | Predicted Winner | Actual Winner | Rank | Probability | Result |
|--------|------------------|---------------|------|-------------|--------|
| 2020-21 | Manchester City | Chelsea | 3 | 18.75% | ❌ |
| 2021-22 | Bayern Munich | Real Madrid | 4 | 12.50% | ❌ |
| 2022-23 | Bayern Munich | Manchester City | 3 | 15.20% | ❌ |
| 2023-24 | Real Madrid | Real Madrid | 1 | 25.60% | ✅ |

*Overall Test Accuracy:* 25% (1/4 correct predictions)

*Average Rank of Actual Winners:* 2.75

---
