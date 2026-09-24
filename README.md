# Students-Academic-Performance
Predictive analytics project analyzing 8,000 students' academic performance across 23 variables (Class 10 to third-year college). Compares Multiple Linear Regression (R²=86.4%) and Logistic Regression (95% precision, 97% recall) models. Predicts Final Score and Passing Status. Built with RStudio and Minitab. M.Sc. Semester 2 course project.

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Models & Results](#models--results)
- [Files Structure](#files-structure)
- [How to Run](#how-to-run)
- [Key Findings](#key-findings)
- [Technologies Used](#technologies-used)
- [Author](#author)

## 📚 Project Overview

This M.Sc. Semester 2 course project focuses on building predictive models for student academic performance. The study compares two powerful machine learning approaches:
1. **Multiple Linear Regression** - for continuous outcome prediction (Final Score)
2. **Logistic Regression** - for binary outcome prediction (Passing Status)

The project demonstrates practical implementation of statistical modeling and machine learning concepts on a real-world educational dataset.

**Institution:** University / College  
**Course:** M.Sc. Semester 2  
**Project Period:** January 2026 - June 2026  
**Dataset Type:** Synthetic educational data

## 📊 Dataset

- **Sample Size:** 8,000 students
- **Total Variables:** 23
- **Target Variables:** 
  - Final Score (continuous - for MLR)
  - Passing Status (binary - for Logistic Regression)
- **Predictor Variables:** 21
- **Student Coverage:** Class 10 through Third Year of College

### Data Characteristics
- Comprehensive student academic records
- Multiple educational levels represented
- Diverse performance metrics included
- Balanced and well-structured data

## 🔬 Methodology

### Approach
1. **Data Exploration & Cleaning**
   - Descriptive statistics
   - Missing value analysis
   - Outlier detection
   - Data visualization

2. **Feature Engineering**
   - Variable selection from 23 total variables
   - 21 predictors identified
   - Correlation analysis
   - Multicollinearity checking

3. **Model Development**
   - Train-test split
   - Model fitting
   - Parameter estimation
   - Coefficient interpretation

4. **Model Validation & Evaluation**
   - Performance metrics calculation
   - Cross-validation
   - Residual analysis
   - Model diagnostics

## 📈 Models & Results

### Model 1: Multiple Linear Regression (MLR)

**Purpose:** Predict Final Score (continuous variable)

**Performance Metrics:**
- **R² (Coefficient of Determination):** 86.4%
- **Interpretation:** The model explains 86.4% of variance in Final Scores
- **Adjusted R²:** Calculated based on degrees of freedom
- **RMSE:** Root Mean Squared Error (model accuracy measure)
- **MAE:** Mean Absolute Error

**Key Insights:**
- Strong predictive power with 86.4% variance explained
- 21 predictor variables effectively capture performance drivers
- Suitable for continuous score prediction

### Model 2: Logistic Regression

**Purpose:** Predict Passing Status (binary outcome: Pass/Fail)

**Performance Metrics:**
- **Precision:** 95%
  - Of predicted passing students, 95% actually pass
  - Minimizes false positives
  
- **Recall:** 97%
  - Identifies 97% of actual passing students
  - Minimizes false negatives
  
- **Accuracy:** High overall correctness rate
- **AUC-ROC:** Model discrimination ability
- **F1-Score:** Harmonic mean of precision and recall

**Key Insights:**
- Excellent at identifying students likely to pass
- High sensitivity (97% recall) catches most potential passers
- High specificity (95% precision) minimizes false alarms
- Balanced model suitable for classification tasks

## 📊 Model Comparison

| Metric | Multiple Linear Regression | Logistic Regression |
|--------|---------------------------|-------------------|
| **Task** | Predict Final Score | Predict Pass/Fail Status |
| **Output Type** | Continuous | Binary (0/1) |
| **Primary Metric** | R² = 86.4% | Precision: 95%, Recall: 97% |
| **Use Case** | Score estimation | Pass/Fail prediction |
| **Strength** | Strong explanatory power | Excellent classification |

## 📁 Files Structure

```
Predictive-Analytics-Project/
├── README.md                          # This file
├── Project_2_Sulagna_Roy.pptx        # Complete presentation
├── Data/
│   ├── raw_data.csv                  # Original 8,000 students dataset
│   ├── data_dictionary.txt           # Variable descriptions
│   └── processed_data.csv            # Cleaned dataset
├── R_Code/
│   ├── 01_data_exploration.R         # EDA and statistics
│   ├── 02_data_preprocessing.R       # Cleaning and feature engineering
│   ├── 03_mlr_model.R                # Multiple Linear Regression
│   ├── 04_logistic_model.R           # Logistic Regression
│   ├── 05_model_evaluation.R         # Performance metrics & comparison
│   └── 06_visualization.R            # Plots and charts
├── Minitab_Files/
│   ├── MLR_Analysis.mpj              # Minitab project for MLR
│   └── Logistic_Analysis.mpj         # Minitab project for Logistic Regression
└── Results/
    ├── MLR_Model_Summary.txt         # MLR coefficients & statistics
    ├── Logistic_Model_Summary.txt    # Logistic regression output
    └── Performance_Metrics.txt       # Comparison results
```

## 🚀 How to Run

### Prerequisites
- **R (version 3.6+)** or **RStudio**
- **Minitab (optional)** for alternative analysis
- **Microsoft PowerPoint** for viewing presentation

### R Installation & Setup

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/predictive-analytics-project.git
cd predictive-analytics-project
```

2. **Install required R packages**
```R
install.packages(c("tidyverse", "caret", "ggplot2", "corrplot", "MLmetrics"))
```

3. **Set working directory**
```R
setwd("your/path/to/project")
```

4. **Run the analysis pipeline**
```R
# Step 1: Explore data
source("R_Code/01_data_exploration.R")

# Step 2: Preprocess data
source("R_Code/02_data_preprocessing.R")

# Step 3: Build MLR model
source("R_Code/03_mlr_model.R")

# Step 4: Build Logistic Regression model
source("R_Code/04_logistic_model.R")

# Step 5: Evaluate and compare models
source("R_Code/05_model_evaluation.R")

# Step 6: Generate visualizations
source("R_Code/06_visualization.R")
```

### Minitab Analysis

1. Open Minitab project files
2. Load the dataset
3. Run pre-configured analysis workflows
4. Generate reports and visualizations

## 📈 Key Findings

### Multiple Linear Regression Insights

**Model Performance:**
- Explains **86.4%** of variance in Final Scores
- Strong predictive capability
- Reliable for score estimation

**Top Predictor Variables** (by importance):
- Previous semester performance
- Class attendance
- Assignment submission rates
- Study hours
- [Additional significant predictors]

**Regression Equation Structure:**
```
Final Score = β₀ + β₁(X₁) + β₂(X₂) + ... + β₂₁(X₂₁) + ε
```

### Logistic Regression Insights

**Model Performance:**
- **Precision: 95%** → Reliable passing predictions
- **Recall: 97%** → Catches almost all at-risk students
- Excellent binary classification capability

**Passing Probability Drivers:**
- GPA threshold effects
- Cumulative performance trends
- Assignment completion patterns
- [Key classification factors]

**Classification Accuracy:**
- True Positive Rate (Sensitivity): 97%
- True Negative Rate (Specificity): 95%
- Overall Classification Accuracy: High

### Cross-Model Insights

1. **Complementary Strengths**
   - MLR: Precise score estimation
   - Logistic: Clear pass/fail decision

2. **Predictor Consistency**
   - Same 21 variables used across both models
   - High correlation between model outcomes
   - Validates variable selection

3. **Business Applications**
   - Score prediction for resource allocation
   - Early intervention for at-risk students
   - Performance forecasting

## 📊 Visualizations Included

The presentation and analysis include:
- Distribution plots of variables
- Correlation heatmaps
- Residual diagnostic plots
- ROC curves for Logistic Regression
- Model comparison charts
- Performance metrics visualization
- Prediction accuracy plots

## 🛠️ Technologies Used

### Statistical Analysis
- **RStudio** - R programming environment
- **R Packages:**
  - `tidyverse` - Data manipulation & visualization
  - `caret` - Model training & evaluation
  - `ggplot2` - Advanced plotting
  - `corrplot` - Correlation visualization
  - `MLmetrics` - Classification metrics

### Alternative Tools
- **Minitab** - Statistical analysis & reporting
- **Microsoft PowerPoint** - Presentation & visualization

### Languages & Tools
- **R** - Statistical computing
- **SQL** (optional) - Data extraction
- **Git** - Version control

## 👩‍🎓 Author

**Sulagna Roy**  
M.Sc. Student  
Course: Predictive Analytics (Semester 2)  
Project Duration: January 2026 - June 2026

## 📝 License

This project is submitted as part of M.Sc. Semester 2 course requirements.

## 📧 Contact & Collaboration

For questions or discussions about this project:
- Email: sulagna01royofficial@gmail.com
- GitHub: https://github.com/sulagna01royofficial
- LinkedIn: www.linkedin.com/in/sulagna01-roy 

## 🎯 Project Achievements

✅ Built and compared two predictive models  
✅ Achieved 86.4% R² on regression model  
✅ Achieved 95% precision and 97% recall on classification  
✅ Analyzed 8,000 student records across 23 variables  
✅ Comprehensive documentation and visualization  
✅ Cross-validated model performance  
✅ Professional presentation delivery  

## 📚 References & Resources

- Predictive Modeling Techniques
- Statistical Learning Theory
- Machine Learning Best Practices
- Educational Data Mining
- Classification & Regression Methods

## 🔄 Future Enhancements

Potential improvements and extensions:
- Ensemble methods (Random Forest, Gradient Boosting)
- Neural Networks for non-linear patterns
- Time-series analysis for performance trends
- Interactive Shiny dashboard for predictions
- Model deployment for real-time prediction
- Feature importance analysis
- Hyperparameter optimization

---

**Last Updated:** June 2026  
**Project Status:** Completed & Submitted  
**Grade Expectation:** Excellent performance metrics achieved

---

## Quick Start Command

```bash
# Clone and run
git clone https://github.com/yourusername/predictive-analytics-project.git
cd predictive-analytics-project
Rscript R_Code/run_all.R
```

**For detailed results, see the PowerPoint presentation: `Project_2_Sulagna_Roy.pptx`**
