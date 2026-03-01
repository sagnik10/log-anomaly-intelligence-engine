# Log Anomaly Intelligence Engine

An end-to-end unsupervised machine learning analytics pipeline for structured logging and monitoring datasets.

This project automatically ingests CSV-based log data, performs statistical profiling, dimensionality reduction, anomaly detection, clustering, feature importance analysis, similarity mapping, and generates a fully formatted multi-page PDF analytical report.

---

## Overview

Modern systems generate massive volumes of logs. Extracting structural insights, identifying anomalies, and understanding behavioral patterns requires automated analytical pipelines.

This repository provides a complete workflow that:

- Loads any structured CSV logging dataset
- Cleans and preprocesses numeric features
- Excludes identifier columns automatically
- Applies scaling and dimensionality reduction
- Detects anomalies using Isolation Forest
- Segments behavior using KMeans clustering
- Computes feature importance via Mutual Information
- Generates similarity-based nearest-neighbor mapping
- Saves trained preprocessing artifacts
- Produces structured visual analytics
- Exports a professional PDF intelligence report

---

## Key Capabilities

### Statistical Profiling
- Automatic numeric feature detection  
- Median imputation for missing values  
- Distribution visualization  
- Correlation matrix generation  

### Dimensionality Reduction
- Principal Component Analysis (PCA)  
- Explained variance visualization  
- 2D projection for structural inspection  

### Anomaly Detection
- Isolation Forest-based anomaly scoring  
- Visual anomaly separation in PCA space  
- Anomaly count reporting  

### Behavioral Segmentation
- KMeans clustering  
- Silhouette score evaluation  
- Cluster distribution visualization  

### Feature Importance
- Mutual Information ranking  
- Non-linear dependency strength estimation  

### Similarity Intelligence
- Cosine similarity nearest-neighbor mapping  
- Top-N similarity recommendations  
- Exportable similarity CSV output  

### Automated Reporting
- Multi-page PDF analytics report  
- Chart-by-chart explanations  
- Clear axis labeling  
- Structured output directory organization  

---

## Repository Structure

    log-anomaly-intelligence-engine/
    │
    ├── main_script.py
    ├── README.md
    │
    └── Output/
        ├── charts/
        ├── models/
        ├── recommendations/
        └── Analytics_Report.pdf

---

## Output Artifacts

### Charts
- PCA Explained Variance  
- PCA Projection  
- Feature Correlation Matrix  
- Feature Distributions  
- Isolation Forest Anomaly Projection  
- Cluster Projection  
- Cluster Distribution  
- Feature Importance  

### Models
- scaler.pkl  
- pca.pkl  

### Data Outputs
- similarity_recommendations.csv  

### Report
- Analytics_Report.pdf  

---

## Installation

Install dependencies:

    pip install numpy pandas matplotlib seaborn scikit-learn reportlab

---

## Usage (Local Execution)

Place your CSV file in the same directory as the script.

Run:

    python main_script.py

Output will be generated inside:

    /Output

---

## Usage (Kaggle)

The pipeline automatically scans:

    /kaggle/input

Outputs are written to:

    /kaggle/working/Output

---

## Design Principles

- Fully unsupervised architecture  
- Identifier column exclusion  
- Adaptive binning for distributions  
- Clean visual formatting  
- Deterministic random state control  
- Modular artifact persistence  
- Production-oriented structure  

---

## Intended Use Cases

- Observability data analysis  
- Monitoring intelligence pipelines  
- Log anomaly exploration  
- Infrastructure behavior segmentation  
- Incident detection research  
- ML experimentation in system telemetry  
- Automated analytics reporting  

---

## Performance Considerations

- Scales efficiently for medium-to-large datasets  
- PCA dimensional compression improves anomaly detection stability  
- Cosine similarity enables high-dimensional nearest-neighbor mapping  
- Vectorized operations minimize processing overhead  

---

## Example Workflow

1. Load log dataset  
2. Remove ID-based leakage variables  
3. Normalize numeric signals  
4. Compress feature space  
5. Detect anomalous behavior  
6. Segment operational patterns  
7. Rank influence drivers  
8. Generate structured report  
9. Export similarity graph  

---

## Future Extensions

- Time-series anomaly modeling  
- Adaptive cluster selection  
- SHAP explainability integration  
- AutoML extension  
- Streamlit dashboard interface  
- Real-time monitoring pipeline  
- Distributed processing integration  

---

## License

MIT License  

---

## Author

Sagnik  
Machine Learning & Systems Intelligence Engineering
