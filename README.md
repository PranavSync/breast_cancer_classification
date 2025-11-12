# Breast Cancer Classification: Logistic Regression vs Random Forest

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-orange)
![ML](https://img.shields.io/badge/Machine-Learning-brightgreen)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

A comprehensive machine learning project comparing Logistic Regression and Random Forest classifiers for breast cancer diagnosis using the Wisconsin Diagnostic Dataset.

## 🎯 Project Overview

This project implements and compares two fundamental classification algorithms to predict breast cancer diagnosis (Malignant vs Benign) based on features computed from digitized images of fine needle aspirates (FNA). The analysis provides insights into model performance, interpretability, and practical considerations for medical applications.

**Key Highlights:**
- Achieved **97% accuracy** with Random Forest and **96% accuracy** with Logistic Regression
- **93% recall** for malignant cases with both models - crucial for medical diagnosis
- **100% precision** with Random Forest - zero false alarms for malignant predictions
- Comprehensive feature importance analysis and model interpretation

## 📊 Dataset

**Source:** Breast Cancer Wisconsin (Diagnostic) Dataset from scikit-learn
- **Samples:** 569
- **Features:** 30 numerical features computed from digitized images
- **Target:** Diagnosis (Malignant/Benign)
- **Classes:** 357 Benign (62.7%), 212 Malignant (37.3%)

## 🏗️ Project Structure

breast_cancer_classification/
├── data/               # Dataset storage
├── notebooks/          # Jupyter notebooks for analysis
├── src/                # Python source code
├── models/             # Saved model files
├── images/             # Visualizations and plots
└── README.md          # Project documentation

## ⚙️ Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/breast_cancer_classification.git
   cd breast_cancer_classification
   ```

2. **Create and activate conda environment**
   ```bash
   conda create -n bc_classification python=3.9 pandas numpy matplotlib seaborn scikit-learn jupyter -y
   conda activate bc_classification
   ```

3. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```
   Navigate to `notebooks/` and open the analysis notebook.

## 🚀 Usage

The project follows a standard machine learning workflow:

1. **Exploratory Data Analysis (EDA)** - Data distribution, correlations, and insights
2. **Data Preprocessing** - Feature scaling and train-test split
3. **Model Training** - Logistic Regression and Random Forest implementation
4. **Model Evaluation** - Comprehensive metrics and visualization
5. **Model Interpretation** - Feature importance and coefficient analysis

## 📈 Results & Findings

### Performance Comparison

| Metric | Logistic Regression | Random Forest |
|--------|---------------------|---------------|
| **Accuracy** | 96% | 97% |
| **Precision (M)** | 97% | 100% |
| **Recall (M)** | 93% | 93% |
| **F1-Score (M)** | 95% | 96% |
| **ROC-AUC** | 0.996 | 0.993 |

### Key Insights

- **Random Forest** demonstrated superior performance with perfect precision (100%) and higher overall accuracy
- Both models achieved the same critical **recall rate (93%)** for malignant cases
- **Feature importance** analysis revealed `worst radius`, `worst perimeter`, and `worst concave points` as most predictive features
- The high **ROC-AUC scores** (≥0.993) indicate excellent model discrimination capability

## 🔍 Model Interpretation

### Random Forest Feature Importance
Top 5 most important features for cancer prediction:
1. `worst radius`
2. `worst perimeter` 
3. `worst concave points`
4. `mean concave points`
5. `worst area`

### Logistic Regression Coefficients
Key features influencing malignant predictions:
- `worst texture` (positive correlation)
- `radius error` (positive correlation) 
- `worst symmetry` (positive correlation)

## 🎯 Business/Medical Implications

- The **93% recall rate** means the model can identify 93% of actual cancer cases
- **100% precision** in Random Forest eliminates unnecessary patient anxiety from false alarms
- Model can serve as a reliable **decision support tool** for medical professionals
- Feature analysis provides clinical insights into which tumor characteristics are most indicative of malignancy

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check [issues page](https://github.com/yourusername/breast_cancer_classification/issues).

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- University of Wisconsin for the Breast Cancer Wisconsin Dataset
- Scikit-learn team for excellent machine learning tools
- Medical researchers working in cancer diagnosis and treatment

### Instructions for Use:

1. Create a new file in your project root folder called `README.md`
2. Copy and paste the entire content above into this file
3. Replace `yourusername` with your actual GitHub username in the clone URL
4. Save the file

### Additional Files to Create:

You might also want to create these files to make your repository more professional:

**1. requirements.txt** (in your project root)\n
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
scikit-learn>=1.0.0
jupyter>=1.0.0

**2. .gitignore** (in your project root)

# Jupyter Notebook
.ipynb_checkpoints

# Environment
bc_classification/
env/

# OS
.DS_Store
Thumbs.db

# IDE
.vscode/
.idea/
