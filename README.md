# 🏠 Smart Home Appliances Manager – Beat the Electricity Bill!

An intelligent household energy-management project that uses real-world electricity consumption data to analyse appliance usage, predict energy consumption, estimate electricity bills, and encourage energy-efficient behaviour through an interactive game.

Team members:
Pradyumna Borate (EC24I2010) | 
Abhilash Sreenivasan (EC24I2006) | 
Sarang Raj P (EC24I2017)

## 📌 Project Overview

Electricity consumption in households depends on several factors, including the appliances being used, their operating durations, and the time of day. Understanding these patterns can help households reduce unnecessary energy consumption and manage electricity expenses more effectively.

**Smart Home Appliances Manager – Beat the Electricity Bill!** aims to develop a data-driven system that analyses household electricity consumption and helps users make smarter decisions about appliance usage.

The project uses the REFIT Electrical Load Measurements dataset, specifically **House 2**, to explore household energy-consumption patterns and develop machine-learning models for energy and electricity-bill prediction.

The project also aims to incorporate an interactive game in which users can manage appliance usage and try to keep their electricity bills within a given budget.

## 🎯 Project Objectives

- Understand and analyse real-world household electricity consumption.
- Explore appliance-wise energy consumption and usage patterns.
- Identify peak consumption periods and possible opportunities for energy savings.
- Perform data cleaning and feature engineering on time-series electricity data.
- Develop machine-learning models to predict household energy consumption.
- Estimate electricity bills using predicted energy consumption.
- Design an interactive game that encourages users to make energy-efficient decisions.

## 📂 Dataset Description

This project uses the **REFIT Electrical Load Measurements dataset**.

REFIT (Personalised Retrofit Decision Support Tools for UK Homes using Smart Home Technology) is a research dataset containing electricity consumption measurements collected from 20 residential households in and around Loughborough, Leicestershire, England, between 2013 and 2015.

The dataset records:

- Whole-house electricity consumption through an aggregate measurement channel.
- Individual appliance consumption through Individual Appliance Monitors (IAMs).
- Active power measurements in Watts.
- Measurements at approximately 8-second intervals.

### Selected Household: House 2

House 2 contains measurements from the following appliances:

| Channel | Appliance |
|---|---|
| Aggregate | Whole-house consumption |
| Appliance 1 | Fridge-Freezer |
| Appliance 2 | Washing Machine |
| Appliance 3 | Dishwasher |
| Appliance 4 | Television |
| Appliance 5 | Microwave |
| Appliance 6 | Toaster |
| Appliance 7 | Hi-Fi System |
| Appliance 8 | Kettle |
| Appliance 9 | Oven Extractor Fan |

**Important:** The aggregate channel represents the overall household consumption. It includes loads that are not individually monitored by the nine appliance channels. Therefore, the sum of the nine appliance readings should not be treated as the total household consumption.

### Dataset Source

Murray, D., Stankovic, L., & Stankovic, V. (2017). *An electrical load measurements dataset of United Kingdom households from a two-year longitudinal study.* Scientific Data, 4, 160122.

DOI: https://doi.org/10.1038/sdata.2016.122

## ⚙️ Project Workflow

The project follows these major stages:

### 1. Data Collection and Understanding

- Load the REFIT House 2 dataset.
- Understand the structure and meaning of each column.
- Identify aggregate and individual appliance measurements.
- Examine timestamps, sampling intervals, missing values, and data quality.

### 2. Data Cleaning

- Handle missing and invalid readings.
- Process duplicate timestamps.
- Examine irregular sampling intervals and missing time periods.
- Prepare a clean dataset for further analysis.

### 3. Feature Engineering

Extract meaningful information from the raw time-series data, including:

- Appliance-wise energy consumption.
- Average and maximum appliance power.
- Time-based features.
- Hourly and monthly consumption features.
- Household energy-consumption statistics.

Energy consumption is estimated by integrating power measurements over time, with appropriate handling of irregular sampling intervals.

### 4. Exploratory Data Analysis (EDA)

Explore household and appliance consumption patterns through:

- Household energy-consumption trends.
- Appliance-wise consumption comparisons.
- Hourly and daily usage patterns.
- Peak power demand analysis.
- Appliance usage distributions.
- Consumption variability and outlier analysis.
- Relationships between appliance usage and household consumption.

### 5. Machine Learning

Develop machine-learning models to predict household energy consumption using appliance-related features.

The intended workflow includes:

1. Preparing input features and prediction targets.
2. Splitting the dataset into training and testing sets.
3. Training suitable regression models.
4. Evaluating model performance.
5. Comparing predictions with actual energy consumption.

The project also aims to use predicted energy consumption to estimate electricity bills.

**Note:** The final models, evaluation metrics, and best-performing algorithm will be documented after model development and testing.

### 6. Interactive Game – Beat the Electricity Bill!

The final application aims to turn household energy management into an interactive experience.

Users will be able to:

- Manage the operation of household appliances.
- Observe how appliance usage affects energy consumption.
- Understand the impact of their decisions on electricity expenses.
- Try to stay within a predefined electricity-bill budget.

The objective is to make energy conservation easier to understand through practical interaction and feedback.

## 🛠️ Technologies Used

The project uses Python and its data-science ecosystem.

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| NumPy | Numerical computations |
| Pandas | Data manipulation and preprocessing |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Scikit-learn | Machine-learning models and evaluation |
| Jupyter Notebook / Google Colab | Development and experimentation |

Additional libraries and frameworks may be included as the interactive application is developed.

## 📊 Model Evaluation

The regression models will be evaluated using suitable performance metrics, including:

- **MAE (Mean Absolute Error):** Measures the average absolute prediction error.
- **MSE (Mean Squared Error):** Measures the average squared prediction error.
- **RMSE (Root Mean Squared Error):** Measures prediction error while retaining the target's units.
- **R² Score:** Indicates how much of the variation in the target is explained by the model.

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone <https://github.com/Pradyumna-Borate/Smart_Home_Appliances_Manager>
```

### 2. Navigate to the Project Directory

```bash
cd Smart-Home-Appliances-Manager
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Obtain the Dataset

Download the REFIT Electrical Load Measurements dataset from its official source.

Place the required House 2 dataset files in the appropriate data directory.

### 5. Run the Notebook

Open the Jupyter Notebook or upload it to Google Colab and execute the cells in sequence.

## ⚠️ Limitations

- The REFIT dataset contains measurements from selected UK households, rather than all types of residential environments.
- The data was collected during 2013–2015, so present-day appliance usage may differ.
- Only selected appliances are individually monitored.
- Missing readings and irregular sampling intervals can affect energy calculations.
- Electricity-bill estimates depend on the tariff assumptions used by the project and may not represent an actual household bill.

## 🔮 Future Improvements

- Experiment with additional regression and time-series forecasting models.
- Improve prediction accuracy through feature selection and hyperparameter tuning.
- Incorporate more household datasets for better generalisation.
- Add configurable electricity tariffs and bill calculations.
- Develop a user-friendly interactive application.
- Introduce appliance scheduling and energy-saving recommendations.
- Expand the game with different difficulty levels, budgets, and household scenarios.

## 👥 Contributors

**Project:** Smart Home Appliances Manager – Beat the Electricity Bill!

**Domain:** Data Science and Machine Learning

## 📜 Acknowledgements

We acknowledge the researchers involved in the REFIT project for making the electrical load measurements dataset available for research and educational purposes.

**Dataset Reference:**  
Murray, D., Stankovic, L., & Stankovic, V. (2017). Scientific Data, 4, 160122.  
https://doi.org/10.1038/sdata.2016.122

---
