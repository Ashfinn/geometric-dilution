# SMOTE Geometric Analysis

A comprehensive research project analyzing the effectiveness of SMOTE (Synthetic Minority Oversampling Technique) and other oversampling methods for handling imbalanced datasets, with a focus on geometric implications and statistical significance.

## 📊 Project Overview

This project evaluates various oversampling techniques for imbalanced classification problems through rigorous statistical analysis, geometric visualization, and performance comparison across multiple datasets and classifiers.

## 🔬 Research Focus

### Oversampling Techniques Analyzed
- **SMOTE** (Synthetic Minority Oversampling Technique)
- **BorderlineSMOTE** - Variant focusing on borderline instances
- **ADASYN** (Adaptive Synthetic Sampling)
- **RandomOverSampler** - Baseline random oversampling
- **No Oversampling** - Control baseline

### Classifiers Evaluated
- **Random Forest** - Tree-based ensemble method
- **Logistic Regression** - Linear classifier
- **Support Vector Machine (SVM)** - Non-linear RBF kernel

### Datasets
- **Wine Quality Dataset** - Highly imbalanced (6.37:1 ratio)
- **Breast Cancer Dataset** - Moderately imbalanced (1.68:1 ratio)

## 📈 Key Metrics

The project evaluates performance using multiple metrics:
- **F1 Score** - Primary metric for imbalanced classification
- **ROC AUC** - Area under ROC curve
- **Precision** - Positive predictive value
- **Recall** - Sensitivity/True positive rate
- **Balanced Accuracy** - Accuracy adjusted for class imbalance
- **Cohen's Kappa** - Inter-rater agreement metric
- **Matthews Correlation Coefficient (MCC)** - Balanced measure

## 🔍 Analysis Methods

### Statistical Testing
- **Paired t-tests** comparing oversampling methods vs. baseline
- **Cohen's d effect sizes** for practical significance assessment
- **Cross-validation** (5-fold stratified) for robust evaluation

### Geometric Analysis
- **PCA visualization** of original vs. synthetic minority samples
- **Precision-Recall trade-off analysis**
- **Imbalance ratio impact analysis**

### Visualizations
- Performance comparison bar plots with error bars
- Confusion matrices for detailed classification results
- ROC and Precision-Recall curves
- Heatmaps showing method-classifier combinations
- Geometric dilution visualizations

## 📊 Key Findings

### Statistical Significance
- **SVM classifier** shows significant improvements with oversampling on Wine Quality dataset (p < 0.001)
- **Random Forest** and **Logistic Regression** show minimal significant differences
- Effect sizes generally small to negligible for most combinations

### Performance Insights
- **Random Forest**: 
  - Wine Quality: RandomOver (+4.80%), ADASYN (+4.47%) show best improvements
  - Breast Cancer: ADASYN (+0.62%) shows slight improvement
- **Imbalance severity** affects oversampling effectiveness
- Higher imbalance ratios benefit more from oversampling techniques

### Geometric Observations
- SMOTE creates synthetic samples in feature space following geometric interpolation
- Borderline SMOTE focuses on difficult boundary cases
- ADASYN adapts density distribution for minority class

## 🛠️ Technical Implementation

### Dependencies
```python
- pandas, numpy, matplotlib, seaborn
- scikit-learn (classification, metrics, preprocessing)
- imbalanced-learn (oversampling techniques)
- scipy (statistical testing)
```

### Project Structure
```
├── smote.ipynb              # Main analysis notebook
├── visualizations/          # Generated visualizations
│   ├── geometric_dilution_simulation_improved.png
│   ├── geometric_dilution_visual_1.png
│   ├── geometric_dilution_visual_2.png
│   └── geometric_dilution_visual_improved.png
├── final.pdf               # Research paper/report
├── output.docx             # Document output
├── Smote_2.pdf            # Additional documentation
└── Smote.pdf              # Research documentation
```

## 🚀 Usage

### Running the Analysis
```python
# Load datasets and run complete evaluation
results, fold_scores = main()

# Generate visualizations
create_comprehensive_visualization(results)

# Perform statistical analysis
for dataset_name in datasets.keys():
    perform_statistical_tests(fold_scores, dataset_name)
```

### Key Functions
- `evaluate_dataset()` - Cross-validation evaluation framework
- `perform_statistical_tests()` - Statistical significance testing
- `calculate_effect_sizes_and_power()` - Effect size analysis
- `create_comprehensive_visualization()` - Publication-ready plots
- `analyze_imbalance_impact()` - Imbalance ratio analysis

## 📋 Research Contributions

1. **Comprehensive Evaluation Framework**: Multi-metric, multi-classifier, multi-dataset analysis
2. **Statistical Rigor**: Proper significance testing with effect size reporting
3. **Geometric Insights**: Visual analysis of synthetic sample generation
4. **Practical Guidelines**: Evidence-based recommendations for oversampling method selection
5. **Reproducible Research**: Complete code and methodology documentation

## 📊 Results Summary

### Random Forest F1 Performance
| Dataset | No Oversampling | RandomOver | SMOTE | BorderlineSMOTE | ADASYN |
|---------|----------------|------------|-------|-----------------|---------|
| WineQuality | 0.604 | 0.633 | 0.609 | 0.609 | 0.631 |
| BreastCancer | 0.965 | 0.968 | 0.966 | 0.963 | 0.971 |

### Statistical Significance (SVM on Wine Quality)
- All oversampling methods show significant improvement (p < 0.001)
- Effect sizes range from small to medium
- BorderlineSMOTE and ADASYN show strongest effects

## 🔮 Future Work

- Analysis of additional datasets with varying imbalance ratios
- Deep learning classifier evaluation
- Cost-sensitive learning comparison
- Ensemble oversampling techniques
- Real-world deployment case studies

## 📄 Publications

This research has been compiled into comprehensive documentation including:
- Technical research papers (PDF format)
- Detailed methodology documentation
- Reproducible analysis notebooks

## 🤝 Contributing

This project serves as a foundation for imbalanced learning research. Contributions for:
- Additional oversampling techniques
- New evaluation metrics
- Extended dataset analysis
- Methodological improvements

## 📚 References

Key techniques and methodologies implemented:
- Chawla, N.V. et al. (2002). SMOTE: Synthetic Minority Over-sampling Technique
- He, H. et al. (2008). ADASYN: Adaptive synthetic sampling approach
- Han, H. et al. (2005). Borderline-SMOTE: A New Over-Sampling Method

---

*This project provides a rigorous, statistical approach to evaluating oversampling techniques for imbalanced classification, contributing valuable insights to the machine learning community.*
