# 🧬 Advanced Analytics of Breast Cancer Genomic Data: Memorial Sloan Kettering Study

## 🚀 Project Overview

The 2018 Memorial Sloan Kettering (MSK) Cancer Center study provided an extensive dataset of 1,918 breast cancer patients. This dataset, comprising clinical outcomes and genomic data on 17,141 genes, offered a valuable opportunity to apply machine learning and advanced analytics to predict patient survival and identify key genetic markers.

## 🛠️ Tools and Libraries Used

### Python Libraries:

- 🐼 Pandas
- 🔢 NumPy
- 📊 Seaborn
- 📈 Matplotlib
- 🤖 Scikit-Learn
- 🕸️ PyViz

### Environment:
- Jupyter Notebook

### Data Source:
- cBioPortal API

## 📊 Data and Exploration

### 📥 Data Acquisition

The data was sourced from cBioPortal, a public cancer genomics platform. The dataset included:

- Patient Demographics
- Tumor Pathology
- Treatment Histories
- Survival Outcomes
- Mutation Statuses for 17,141 Genes

### Sample Dataset Visualization
Overview of patient demographic distribution and gene mutation coverage.

### 🔍 Exploration Questions

Key questions explored in this analysis included:

- 📈 What are the most frequently mutated genes?
- 🧪 How do mutations correlate with patient survival?
- 🤖 Which machine learning models best predict survival outcomes?
- 🔗 What patterns of gene co-occurrence or mutual exclusivity exist?

#### ❓ Question 1: What are the most frequently mutated genes?

To identify the most frequently mutated genes, mutation counts were aggregated and visualized.

```python
mutation_counts = data['Gene'].value_counts()
sns.barplot(x=mutation_counts[:10].index, y=mutation_counts[:10].values)
```

**Mutation Frequency of Top 10 Genes**

Boxplot of Mutation Frequencies Across Key GenesVisualizing distribution and variability in mutation frequencies.

**🔍 Insight:** PIK3CA and TP53 mutations were the most prevalent, highlighting their potential as key biomarkers.

#### ❓ Question 2: How do mutations correlate with survival?

Machine learning models were trained to predict patient survival based on genomic features. The following models were evaluated:

- 🌲 Random Forest – Accuracy: 85%, AUC: 0.87
- 📈 Support Vector Machine (SVM) – Accuracy: 83%, AUC: 0.86
- 🎲 Naive Bayes – Accuracy: 78%, AUC: 0.80

```python
from sklearn.ensemble import RandomForestClassifier
model = RandomForestClassifier()
model.fit(X_train, y_train)
```

**ROC Curve Comparison of Models**

Feature Importance Plot (Random Forest)Key genetic features influencing survival predictions.

**🏆 Conclusion:** Random Forest performed best, with TP53, PIK3CA, and BRCA1/2 emerging as top predictors.

#### ❓ Question 3: What patterns of gene co-occurrence exist?

Relational data mining techniques were employed to identify gene-gene interactions. Co-occurrence patterns were visualized using heatmaps.

```python
sns.heatmap(co_occurrence_matrix, cmap="coolwarm")
```

**Gene Co-occurrence Heatmap**

Network Visualization of Gene InteractionsVisualizing complex gene interaction networks.

**🔗 Key Insight:** CDH1 and PIK3CA mutations co-occur frequently, while TP53 mutations are mutually exclusive with PIK3CA.

## 🛠️ Challenges and Solutions

- 📏 High Dimensionality: Feature selection reduced overfitting risks.
- ⚖️ Class Imbalance: Stratified sampling ensured balance between survival classes.
- 🔍 Interpretability: Feature importance and decision tree visualization enhanced model transparency.

**Decision Tree Visualization (Random Forest)** A detailed view of the decision paths leading to survival predictions.

## 🔮 Future Work

- 📈 Expand Analysis: Apply this workflow to datasets from other cancers.
- 🧬 Multi-Omic Data: Integrate genomic, transcriptomic, and proteomic datasets.
- 🏥 Clinical Tools: Develop AI-driven tools to support oncologists.

## 🏁 Conclusion

This project demonstrated how advanced analytics can unlock critical insights from breast cancer genomic data. By applying machine learning and data visualization, significant gene mutations and co-occurrence patterns were identified. Future work aims to expand and translate these insights into clinical applications, driving advancements in precision oncology.

💡 Stay tuned for further updates and open-source code releases!
