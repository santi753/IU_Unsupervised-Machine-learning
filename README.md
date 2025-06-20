<!-- Project banner -->
![Mental Health in Tech Survey Analysis](github-header-image.png)
# Mental Health in Tech Survey Analysis

A comprehensive data science project analyzing mental health patterns in technology workplaces using unsupervised machine learning to identify distinct employee segments for targeted HR interventions.

## 📋 Project Overview

This project transforms complex mental health survey data into actionable insights for HR departments in technology companies. Using clustering analysis, we identify three distinct employee segments based on mental health needs, workplace support, and employment characteristics.

Key Findings

- 51% High Mental Health Needs: Traditional employees requiring comprehensive support
- 33% Low Mental Health Needs: Healthy workforce benefiting from preventive programs
- 16% Self-Employed Moderate Needs: Freelancers with unique support requirements

## 🎯 Business Impact

The analysis provides HR leadership with:

- Data-driven employee segmentation for targeted interventions
- Clear resource allocation priorities (60% for high-need, 25% prevention, 15% self-employed)
- Evidence that untreated mental health issues cause 10x more work interference
- Strategies to address the 40% of employees who fear career damage from disclosure

## 📊 Dataset

- Source: Mental Health in Tech Survey 2016
- Original Size: 1,433 responses across 63 variables
- Final Dataset: 835 US-based respondents with 43 features

### Key Variables

- Demographics (age, gender, employment type)
- Mental health status (past/current disorders, treatment history)
- Workplace support (benefits, resources, company culture)
- Stigma and disclosure concerns
- Work performance impact

## 🛠️ Installation & Setup

### Prerequisites

- **Python 3.9+** (Python 3.10 or 3.11 recommended for optimal performance)
- **pip package manager** (usually comes pre-installed with Python)

> **Note:** To verify your Python and pip installation, run:
> ```bash
> python --version
> pip --version
> ```
> If pip is not installed, follow the [official pip installation guide](https://pip.pypa.io/en/stable/installation/).

### Required Libraries

Install all required dependencies using pip:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl scipy jupyter
```

## 🚀 How to Run

### Step 1: Clone the Repository

```bash
git clone https://github.com/santi753/IU_Unsupervised-Machine-learning.git
cd IU_Unsupervised-Machine-learning
```

### Step 2: Verify Dataset

The dataset `mental-heath-in-tech-2016_20161114.csv` is already included in the repository or at https://www.kaggle.com/datasets/osmi/mental-health-in-tech-2016.

### Step 3: Run the Analysis

#### Option A: Jupyter Notebooks (Recommended)

1. Start Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

2. Open and run the notebooks in the following order:
   - `Preprocessing.ipynb` (data cleaning and preprocessing)
   - `Clustering.ipynb` (clustering analysis and results)

#### Option B: Python Scripts

If you prefer to run the notebooks as Python scripts:

1. Convert notebooks to Python scripts:
   ```bash
   jupyter nbconvert --to script Preprocessing.ipynb
   jupyter nbconvert --to script Clustering.ipynb
   ```

2. Run the scripts in order:
   ```bash
   python Preprocessing.py  # Data cleaning and preprocessing
   python Clustering.py      # Clustering analysis and results
   ```

### Step 4: View Results

The analysis generates the following outputs:

- `mental_health_features_cleaned.xlsx` - Cleaned dataset
- `mental_health_scaled_final.csv` - Preprocessed features  
- Various visualization plots saved as PNG files
- Detailed cluster analysis and HR recommendations

## 🔍 Analysis Pipeline

1. Data Preprocessing (Preprocessing.ipynb)

- Geographic Filtering: US-based respondents only
- Data Cleaning: Age validation (18-80), gender standardization
- Feature Selection: Reduced from 63 to 43 relevant variables
- Missing Value Handling: Strategic imputation using mode/median
- Encoding: Ordinal and label encoding for categorical variables
- Scaling: StandardScaler for clustering compatibility

2. Clustering Analysis (Clustering.ipynb)

- Algorithm Testing: K-Means, Agglomerative, Gaussian Mixture Models
- Dimensionality Reduction: t-SNE for visualization
- Model Selection: Agglomerative Clustering (3 clusters, silhouette score: 0.484)
- Validation: Stability testing across multiple initializations
- Profiling: Detailed cluster characterization and interpretation

## 📈 Key Results

### Cluster Profiles

🔴 Cluster 0 - High Mental Health Needs (51%)

- 95% have sought treatment, 73% currently have disorders
- 62% report frequent work interference when untreated
- Strong family history (70%) suggests genetic/environmental factors
- Recommendation: Comprehensive support programs, enhanced access, crisis protocols

🟢 Cluster 1 - Low Mental Health Needs (33%)

- Only 5% current disorders, 17% treatment history
- Minimal work interference, represents healthy workforce
- Male-dominated (79%) suggesting potential underreporting
- Recommendation: Preventive wellness programs, mental health literacy

🟡 Cluster 2 - Self-Employed Moderate Needs (16%)

- 98.5% self-employed with moderate burden (51% current disorders)
- 100% benefits access (self-managed) but highest stigma concerns
- High remote work (48%) and flexibility needs
- Recommendation: Flexible solutions, virtual communities, financial support

## 🌐 Universal Findings

- Stigma Impact: ~40% across all clusters fear career damage
- Treatment Effectiveness: 10x reduction in work interference when treated
- Communication Gap: Many don't understand available benefits
- Cultural Issues: Most employers never formally discuss mental health

## 🔧 Technical Notes

- Clustering Approach: t-SNE dimensionality reduction improved cluster interpretability
- Validation Method: 7-seed stability testing (mean ARI = 0.638) confirms robustness
- Scaling: StandardScaler essential for distance-based algorithms
- Feature Engineering: Ordinal encoding preserves meaningful variable relationships

## Contributing

If you find any issues or have feature requests, please open an issue on our Github repository. 
Code contributions in the form of Pull Requests are also welcome. 

## License

This project is licensed under the MIT License.

MIT License

## Support

If you have questions or need further guidance, please reach out to santi_753@hotmail.com

