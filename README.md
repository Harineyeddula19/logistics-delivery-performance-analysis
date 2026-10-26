# Logistics Delivery Performance Analysis and Delivery Time Prediction

## Project Overview

This project was developed as part of a Logistics Data Analyst Internship. It focuses on analyzing food delivery performance, understanding factors associated with delivery duration, and applying machine learning techniques to predict delivery time.

The project follows a data analytics workflow involving data quality assessment, data cleaning, exploratory data analysis (EDA), visualization, regression modeling, model evaluation, and hyperparameter tuning. Python-based analytical techniques were used to identify patterns in delivery time and explore how traffic, distance, vehicle type, order type, and other available variables relate to delivery performance.

## Objectives

- Analyze delivery duration and its distribution.
- Examine the relationship between delivery time and distance.
- Compare delivery performance across traffic levels, vehicle types, and order types.
- Identify and document missing values and data quality issues.
- Develop visualizations to support data-driven interpretation.
- Train and compare regression models for delivery-time prediction.
- Evaluate model performance using MAE, RMSE, and R².
- Apply cross-validation and hyperparameter tuning.
- Propose practical recommendations while documenting analytical limitations.

## Dataset

**Dataset:** Food Delivery Dataset for Delivery Time Prediction

**Source:** [Zenodo Dataset Record](https://zenodo.org/records/18370027)

The working dataset contains 10,001 rows and 17 columns, including delivery-person attributes, location coordinates, order type, vehicle type, weather conditions, traffic level, distance, and delivery time.

A total of 961 records had missing values in the target variable, Delivery Time. These records were excluded from supervised modeling, leaving 9,040 records for model development and evaluation.

The units of Delivery Time and Distance have not been independently verified. Dataset usage terms should be checked before redistributing the original data or publishing it in this repository.

## Tools and Technologies

- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
- Jupyter Notebook
- Git and GitHub

## Project Workflow

### Week 1: Strategic Planning and Data Exploration

- Defined the business problem and project objectives.
- Identified the key areas for delivery performance analysis.
- Reviewed the dataset structure and established the project roadmap.

### Week 2: Data Cleaning and Preprocessing

- Inspected missing values and data quality issues.
- Standardized categorical values.
- Checked data types and numerical ranges.
- Prepared the cleaned dataset for exploratory analysis and modeling.

### Week 3: Exploratory Data Analysis and Visualization

- Analyzed delivery-time distributions and descriptive statistics.
- Examined the relationship between distance and delivery time.
- Compared delivery times across traffic levels, vehicle types, and order types.
- Created visualizations and documented analytical findings.

**Key EDA findings:**

- Mean recorded Delivery Time: 37.66.
- Median recorded Delivery Time: 35.98.
- Mean recorded Distance: 14.21.
- Correlation between Distance and Delivery Time: +0.869.
- Average recorded delivery time increased from 13.89 for Very Low traffic to 62.26 for Very High traffic.

These results describe patterns in the dataset and do not establish causation.

### Week 4: Predictive Modeling and Evaluation

- Selected relevant numerical and categorical predictors.
- Prepared the data using imputation and one-hot encoding pipelines.
- Split the data into training and testing sets using an 80:20 ratio.
- Trained Linear Regression and Random Forest Regression models.
- Evaluated model performance using MAE, RMSE, and R².
- Applied three-fold cross-validation and randomized hyperparameter tuning.
- Examined feature importance, actual-versus-predicted values, and residuals.
- Documented recommendations, limitations, and possible future improvements.

## Model Performance Results

The following results were obtained on a held-out test set of 1,808 records.

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Linear Regression | 3.199 | 4.962 | 0.908 |
| Baseline Random Forest | 2.345 | 3.216 | 0.962 |
| Tuned Random Forest | 2.351 | 3.215 | 0.962 |

The baseline Random Forest model achieved the lowest MAE and outperformed Linear Regression on the reported test metrics. Hyperparameter tuning produced similar results without a meaningful improvement over the baseline model.

The reported results come from a single random train/test split and should not be treated as a guarantee of real-world performance.

## Key Analytical Insights

- Distance showed a strong positive correlation with recorded delivery time.
- Average delivery time increased across the recorded traffic categories.
- Vehicle type and order type showed differences in average recorded delivery time.
- Traffic-level features and Distance were among the most influential predictors in the fitted Random Forest model.
- Prediction and residual plots helped identify variation in model errors.

Feature importance indicates predictive association, not proof of causation.

## Recommendations

- Investigate traffic-aware delivery planning when reliable traffic information is available before dispatch.
- Review longer-distance deliveries and evaluate feasible route alternatives.
- Monitor prediction errors across traffic levels, vehicle types, order types, and locations.
- Verify the units of Delivery Time and Distance before operational use.
- Confirm that all model predictors are available at the time a prediction would be made.
- Conduct time-based or geographic validation before considering real-world deployment.

These recommendations are proposed next steps. The project has not been deployed as a live logistics optimization system and does not claim measured cost savings or improvements in on-time delivery.

## Expected Outcomes and Deliverables

- Documented data cleaning and preprocessing workflow.
- Exploratory data analysis and visualizations.
- Comparison of regression models for delivery-time prediction.
- Model evaluation and hyperparameter tuning results.
- Feature-importance analysis and residual diagnostics.
- Technical project report and reproducible analysis notebooks.
- Recommendations for further logistics performance analysis.

## Limitations and Future Improvements

- Delivery Time and Distance units require verification.
- Random train/test splitting may not fully represent future deliveries.
- Predictor availability at dispatch must be verified.
- Hyperparameter tuning covered a limited search space.
- The model has not been evaluated in a live operational environment.
- Further validation is required to understand model performance across different periods and locations.

Future improvements could include time-based validation, geographic holdout testing, additional regression models, prediction uncertainty analysis, and model monitoring.

## Repository Structure

```text
logistics-delivery-performance-analysis/
│
├── data/
├── notebooks/
│   ├── Week3_Logistics_EDA.ipynb
│   └── Week4_Predictive_Modeling.ipynb
├── outputs/
├── reports/
└── README.md
```

The folder structure above is illustrative. Update it to match the files actually present in the GitHub repository.

## How to Run the Project

### Prerequisites

Install Python and Jupyter Notebook, or use Anaconda.

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl jupyter
```

### Steps

1. Clone or download the GitHub repository.
2. Obtain the dataset from the source, subject to its usage terms.
3. Place the dataset and cleaned data in the appropriate project folders.
4. Check and update file paths in the notebooks if necessary.
5. Open Jupyter Notebook.
6. Run the Week 3 EDA notebook to explore the data.
7. Run the Week 4 predictive modeling notebook to train and evaluate the models.

## Author

**Yeddula Harine**

Logistics Data Analyst Internship Project

**GitHub Repository:** [Logistics Delivery Performance Analysis and Delivery Time Prediction](https://github.com/Harineyeddula19/logistics-delivery-performance-analysis)
