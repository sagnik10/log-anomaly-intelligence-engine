# Log Anomaly Intelligence Engine

An end-to-end unsupervised machine learning analytics pipeline for structured logging and monitoring datasets.

This project analyzes operational telemetry data, detects anomalies, segments behavioral patterns, and generates a fully structured multi-page PDF intelligence report — entirely from a single CSV input.

---

## Overview

Modern systems generate high-volume logging and monitoring data. Extracting meaningful insights from this data requires structured statistical analysis and machine learning.

This repository provides a local, self-contained analytics engine that:

- Automatically reads CSV log data
- Detects numeric behavioral features
- Excludes identifier columns
- Performs dimensionality reduction
- Detects anomalies using Isolation Forest
- Segments behavior using KMeans clustering
- Computes feature importance using Mutual Information
- Generates similarity-based record mapping
- Produces professional visual analytics
- Exports a structured PDF report
- Saves trained preprocessing artifacts

No Kaggle dependency. Fully local execution.

---

## Project Structure

```
LOGGING_AND_MONITORING/
│
├── Analyzer.py
├── logging_monitoring_anomalies.csv
│
└── Output/
    ├── charts/
    ├── models/
    ├── recommendations/
    └── Analytics_Report.pdf
```

---

## What The Pipeline Does

### 1. Data Processing
- Loads CSV automatically from project directory
- Normalizes column names
- Removes ID-like columns from modeling
- Handles missing numeric values via median imputation

### 2. Statistical Profiling
- Feature distribution analysis
- Correlation matrix generation
- Adaptive histogram binning
- Density overlays

### 3. Dimensionality Reduction
- Principal Component Analysis (PCA)
- Cumulative explained variance visualization
- 2D structural projection

### 4. Anomaly Detection
- Isolation Forest algorithm
- PCA-space anomaly visualization
- Automatic anomaly count

### 5. Behavioral Segmentation
- KMeans clustering (k=4)
- Silhouette score evaluation
- Cluster projection visualization
- Cluster population distribution

### 6. Feature Importance
- Mutual Information ranking
- Non-linear dependency measurement

### 7. Similarity Intelligence
- Cosine similarity nearest neighbors
- Top-5 similar record recommendations
- Exportable similarity mapping CSV

### 8. Automated Reporting
- Multi-page PDF report
- Structured section formatting
- Axis labeling for every figure
- Per-chart explanation text
- Clean output directory structure

---

## Generated Output

### Charts (Output/charts)
- PCA Explained Variance
- PCA Projection
- Feature Correlation Matrix
- Individual Feature Distributions
- Isolation Forest Projection
- Cluster Projection
- Cluster Distribution
- Feature Importance

### Models (Output/models)
- scaler.pkl
- pca.pkl

### Recommendations (Output/recommendations)
- similarity_recommendations.csv

### Report
- Analytics_Report.pdf

---

## Installation

Install required dependencies:

```
pip install numpy pandas matplotlib seaborn scikit-learn reportlab
```

---

## Usage (Local Only)

1. Place your CSV file inside the project directory.
2. Ensure the script name is `Analyzer.py`.
3. Run:

```
python Analyzer.py
```

4. Check the `Output/` directory for results.

---

## Design Philosophy

- Fully unsupervised architecture
- Clean separation of input and output
- Deterministic reproducibility
- Minimal configuration required
- Automatic feature detection
- Visual-first intelligence reporting
- Production-oriented folder structure

---

## Use Cases

- Log anomaly investigation
- Monitoring intelligence analysis
- Infrastructure behavior segmentation
- Incident pattern exploration
- Operational telemetry research
- ML experimentation on system data

---

## Example Analytical Flow

1. Load operational logs  
2. Clean and normalize signals  
3. Reduce dimensionality  
4. Detect anomalous behavior  
5. Segment structural patterns  
6. Rank influence features  
7. Map behavioral similarity  
8. Generate intelligence report  

---

## Future Enhancements

- Time-series anomaly modeling
- Adaptive cluster selection
- SHAP explainability integration
- Dashboard interface (Streamlit)
- Real-time monitoring pipeline
- AutoML experimentation layer

---

## License

MIT License

---

## Author

Sagnik  
Machine Learning & Systems Intelligence Engineering
