# Advanced Analytics of Breast Cancer Genomic Data: Memorial Sloan Kettering Study

## Project Overview

The 2018 Memorial Sloan Kettering (MSK) Cancer Center study provided an extensive dataset of 1,918 breast cancer patients. This dataset, comprising clinical outcomes and genomic data on 17,141 genes, offered a valuable opportunity to apply machine learning and advanced analytics to predict patient survival and identify key genetic markers.

## Tools and Libraries Used

- **Python Libraries:**
  - Pandas
  - NumPy
  - Seaborn
  - Matplotlib
  - Scikit-Learn
  - PyViz

- **Environment:** Jupyter Notebook  
- **Data Source:** cBioPortal API

## Data and Exploration

### Data Acquisition

The data was sourced from cBioPortal, a public cancer genomics platform. The dataset included:
- Patient Demographics
- Tumor Pathology
- Treatment Histories
- Survival Outcomes
- Mutation Statuses for 17,141 Genes

### Exploration Questions

Key questions explored in this analysis included:
1. What are the most frequently mutated genes?
2. How do mutations correlate with patient survival?
3. Which machine learning models best predict survival outcomes?
4. What patterns of gene co-occurrence or mutual exclusivity exist?

### Insights

- **Most Frequently Mutated Genes:** PIK3CA and TP53 mutations were the most prevalent, highlighting their potential as key biomarkers.
- **Correlation with Survival:** Random Forest performed best, with TP53, PIK3CA, and BRCA1/2 emerging as top predictors.
- **Gene Co-occurrence Patterns:** CDH1 and PIK3CA mutations co-occur frequently, while TP53 mutations are mutually exclusive with PIK3CA.

## Challenges and Solutions

- **High Dimensionality:** Feature selection reduced overfitting risks.
- **Class Imbalance:** Stratified sampling ensured balance between survival classes.
- **Interpretability:** Feature importance and decision tree visualization enhanced model transparency.

## Future Work

- Expand Analysis: Apply this workflow to datasets from other cancers.
- Multi-Omic Data: Integrate genomic, transcriptomic, and proteomic datasets.
- Clinical Tools: Develop AI-driven tools to support oncologists.

## Conclusion

This project demonstrated how advanced analytics can unlock critical insights from breast cancer genomic data. By applying machine learning and data visualization, significant gene mutations and co-occurrence patterns were identified. Future work aims to expand and translate these insights into clinical applications, driving advancements in precision oncology.

Stay tuned for further updates and open-source code releases!