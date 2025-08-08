**K-Means Clustering on Air Pollution Data**
**Project Overview**
Air pollution is a major environmental and public health challenge, contributing to serious illnesses such as heart disease, lung cancer, pneumonia, and bronchitis. According to the World Health Organization (WHO), it causes approximately 2.4 million deaths annually.

Beyond its health impacts, air pollution drives smog formation, acid rain, ozone layer depletion, and global warming.

This project applies the K-Means clustering algorithm to air pollution data, grouping similar pollutant profiles to uncover patterns and support further environmental analysis.

The dataset includes measurements of five major pollutants:

SO₂ – Sulfur Dioxide

NO₂ – Nitrogen Dioxide

O₃ – Ozone

PM₂.₅ – Particulate Matter ≤ 2.5 μm

PM₁₀ – Particulate Matter ≤ 10 μm

**Objective**
To perform K-Means clustering on air pollution data to:

Identify patterns among pollutant concentrations

Group records into meaningful clusters

Understand correlations between pollutants

**Dataset**
Rows: 3,347

Columns: 5 (SO₂, NO₂, O₃, PM₂.₅, PM₁₀)

Missing Values: None


**Methodology**
1 Data Preprocessing
Checked for missing values (none found)

Standardized features using StandardScaler from scikit-learn

2 Exploratory Data Analysis (EDA)
Used .info() and .describe() for dataset overview

Created a correlation heatmap for pollutant relationships

Plotted distribution histograms for each pollutant

3 Optimal k Selection
Applied the Elbow Method with KneeLocator (from the kneed library)

Computed Sum of Squared Errors (SSE) for k = 1 to 10

Chose k = 3 as the optimal number of clusters

4 Model Training & Visualization
Trained KMeans from scikit-learn with k = 3

Reduced dimensions using PCA (2 components)

Visualized clusters in 2D space

5 Exporting Results
Saved clustered data into an Excel file with pandas

Exported file to the working directory

**Results & Insights**
Pollutant Levels
SO₂: Lowest average, minimum, and maximum concentrations

PM₁₀: Highest average and maximum concentrations

O₃: Highest minimum concentration

Correlations
PM₂.₅ & PM₁₀ → 0.87 (very high)

PM₂.₅ & NO₂ → 0.67

PM₁₀ & NO₂ → 0.64

NO₂ & SO₂ → 0.51

O₃ → Not correlated with other pollutants

Cluster Analysis
k = 3 yielded the most meaningful grouping

PCA visualization showed clear separation between clusters

**Technologies Used**
Python

Libraries:

NumPy, Pandas

Matplotlib, Seaborn

scikit-learn

kneed

os

