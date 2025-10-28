# 🔧 Predictive Maintenance using PySpark

![PySpark](https://img.shields.io/badge/PySpark-2.0.2-orange?logo=apache-spark)
![Python](https://img.shields.io/badge/Python-2.7.5-blue?logo=python)
![ML](https://img.shields.io/badge/Machine%20Learning-Classification-green)
![Status](https://img.shields.io/badge/Status-Production%20Ready-success)

> Built an end-to-end machine learning pipeline to predict equipment failures 7 days in advance using distributed computing with PySpark. Processed 2M+ records across 1,900 machines to achieve high-precision failure prediction.

## 📊 Project Stats

| Metric | Value |
|--------|-------|
| 📦 **Dataset Size** | 1.3 GB / ~2M records |
| 🏭 **Machines Monitored** | 1,900 devices |
| ⏱️ **Time Period** | 4 years |
| 📈 **Features (Raw)** | 172 columns |
| 🔄 **Rolling Features** | 1,150 engineered |
| 🎯 **Final Features** | 140 (post-PCA) |
| 🎚️ **Prediction Window** | 7 days ahead |
| 📉 **Class Imbalance** | 98.5% / 1.5% |
| 🎯 **Model** | Random Forest (optimized) |

## 🚀 Key Technical Achievements

### 🔨 Data Engineering
- ✅ Resolved Spark CSV parsing issues with null handling
- ✅ Implemented comprehensive data quality pipeline
- ✅ Reduced dimensionality using PCA (172 → 50 components)
- ✅ Created 1,150 rolling statistics features (5 windows × 46 features × 5 stats)

### ⚡ Performance Optimization
- ✅ Overcame Spark StackOverflow errors via workload chunking
- ✅ Optimized join operations using `coalesce()` vs `repartition()`
- ✅ Leveraged Parquet format for schema preservation
- ✅ Utilized 32-core VM with full CPU utilization

### 🤖 Machine Learning
- ✅ Implemented over-labeling technique for early warning (7-day window)
- ✅ Applied stratified down-sampling (1:10 ratio) for class balance
- ✅ Built Random Forest & Gradient-Boosted Tree classifiers
- ✅ Performed grid search with 3-fold cross-validation
- ✅ Optimized for precision over recall (business cost-driven)

## 📓 Notebook Structure

| Notebook | Focus Area | Key Outputs |
|----------|-----------|-------------|
| **01_DataCleansing_FeatureEngineering** | Data cleaning, EDA, feature creation | 172 → 140 features |
| **02_FeatureEngineering_RollingCompute** | Time-series rolling statistics | +1,150 temporal features |
| **03_Labeling_FeatureSelection_Modeling** | ML pipeline, model training & tuning | Production-ready model |

## 🛠️ Tech Stack

```
Big Data:      Apache Spark 2.0.2, PySpark
ML/DL:         Spark MLlib, scikit-learn
Processing:    32-core Linux DSVM (448 GB RAM)
Storage:       Azure Blob Storage, Parquet
Visualization: Matplotlib, Seaborn
```

## 🎯 Business Impact

- 🔍 **Proactive Maintenance**: 7-day advance warning enables resource planning
- 💰 **Cost Optimization**: High precision minimizes false positive costs
- ⚙️ **Scalable**: Architecture supports multi-TB datasets
- 📦 **Production Ready**: Saved optimized model for deployment

## 📈 Model Performance

- **Algorithm**: Random Forest (100 trees, hyperparameter tuned)
- **Optimization Metric**: Weighted Precision
- **Evaluation**: ROC-AUC, Precision-Recall, F1-Score
- **Validation**: 3-fold cross-validation with temporal split

---

⭐ **Built with scalability and production deployment in mind**