# K-Means Clustering on Air Pollution Data

## Project Overview
Air pollution is a major environmental and public health issue, contributing to diseases such as heart disease, lung cancer, pneumonia, and bronchitis. The World Health Organization (WHO) estimates that air pollution causes 2.4 million deaths annually.  
Beyond health impacts, air pollution also contributes to smog, acid rain, ozone layer depletion, and global warming.  
This project applies the **K-Means clustering algorithm** to air pollution data to group similar pollutant profiles together for better understanding and analysis.

The dataset contains measurements of five major pollutants:
- **SO₂** (Sulfur Dioxide)
- **NO₂** (Nitrogen Dioxide)
- **O₃** (Ozone)
- **PM₂.₅** (Particulate Matter ≤ 2.5μm)
- **PM₁₀** (Particulate Matter ≤ 10μm)

## Objective
To perform **K-Means clustering** on air pollution data to:
- Identify patterns among pollutants
- Group regions/days into meaningful clusters
- Understand pollutant correlations

## Dataset
- **Rows:** 3,347
- **Columns:** 5 (SO₂, NO₂, O₃, PM₂.₅, PM₁₀)
- **Missing Values:** None
- **Source:** Provided as part of Postgraduate Diploma coursework

## Methodology

### 1. Data Preprocessing
- Checked for missing values (none found)
- Scaled features using StandardScaler from scikit-learn

### 2. Exploratory Data Analysis (EDA)
- .info() and .describe() for dataset summary
- Correlation heatmap for pollutant relationships
- Distribution plots for each pollutant using histograms

### 3. Optimal k Selection
- Used **Elbow Method** with KneeLocator (from the kneed library)
- Calculated Sum of Squared Errors (SSE) for k = 1 to 10
- Chose **k = 3** as the optimal number of clusters

### 4. Model Training
- Applied KMeans from scikit-learn with k = 3
- Performed dimensionality reduction using PCA (2 components)
- Visualized clusters in 2D space

### 5. Exporting Results
- Saved clustered data into an Excel file using pandas
- Exported file to working directory

## Results & Insights
- **Pollutant Levels:**
  - SO₂: Lowest average, min, and max concentrations
  - PM₁₀: Highest average and max concentrations
  - O₃: Highest minimum concentration
- **Correlations:**
  - PM₂.₅ & PM₁₀: **0.87** (high correlation)
  - PM₂.₅ & NO₂: **0.67**
  - PM₁₀ & NO₂: **0.64**
  - NO₂ & SO₂: **0.51**
  - O₃: Not correlated with other pollutants
- **Cluster Analysis:**
  - **k = 3** provided the best grouping
  - PCA visualization clearly shows separation of pollutant profiles

##  Technologies Used
- Python
- **Libraries:**
  - NumPy, Pandas
  - Matplotlib, Seaborn
  - scikit-learn
  - kneed
  - os



