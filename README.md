# Hidden-NB
A simple implementation of Hidden Naive Bayes. Doing a comparison with Naive Bayes using a lot of databases.


# Project: Hidden Naive Bayes (HNB)

## Description
This project replicates the paper *"A Novel Bayes Model: Hidden Naive Bayes"* by Liangxiao Jiang, Harry Zhang, and Zhihua Cai, implementing the Hidden Naive Bayes (HNB) model in Python. Additionally, it introduces a graph to visualize relationships between attributes in the datasets, identifying hidden parent attributes. This feature was not included in the original paper's code.

## Objectives
1. Reproduce the accuracies reported in the paper for various datasets.
2. Implement a visualization to identify relationships between attributes using hidden parent graphs.
3. Compare the performance of HNB against the Naive Bayes (NB) model.

## Datasets
29 datasets with various characteristics were used, following a detailed preprocessing pipeline:
- Imputation of missing values.
- Discretization of numerical attributes using Weka's `Discretize` filter.
- Removal of irrelevant or noisy attributes.
- No subsampling was performed to ensure consistent results.

## Methodology
- **Hidden Naive Bayes (HNB):** An extension of Naive Bayes that relaxes the conditional independence assumption by introducing hidden parent attributes.
- **Implementation:** Developed in Python using libraries like NumPy, pandas, scikit-learn, and networkx.
- **Validation:** Evaluated using K-fold cross-validation with metrics such as accuracy and conditional log-likelihood (CLL).

## Results
- In most cases, the Naive Bayes (NB) model outperformed HNB in terms of accuracy and computational simplicity.
- HNB showed significant limitations on datasets with predominantly binary or ternary attributes due to less informative conditional distributions and overfitting issues.
- The generated graphs of attribute relationships provided a useful tool to interpret the relative importance of features.

## Conclusions
1. **HNB Advantages:** Its ability to capture hidden dependencies can be beneficial in specific cases.
2. **Limitations:** HNB is sensitive to datasets with low variability in attributes and heavily relies on tuning the smoothing factor (ϵ).
3. **Recommendations:** 
   - Dynamically adjust the smoothing factor ϵ.
   - Optimize preprocessing and data discretization.
   - Explore improvements in identifying hidden parent attributes.

## Visualizations
Graphs were generated for several datasets, highlighting key relationships between attributes based on the calculated weights (`Wij`).

## Tools Used
- Python: Model implementation and data preprocessing.
- NetworkX: Visualization of attribute relationship graphs.
- Weka: Initial data imputation and discretization.

## Author
**Carlos Alexis Barrios Bello**  
Master's Student in Artificial Intelligence, Universidad Veracruzana.  
zS23000636@estudiantes.uv.mx

## References
1. Jiang, L., Zhang, H., & Cai, Z. (2009). A Novel Bayes Model: Hidden Naive Bayes. *IEEE Transactions on Knowledge and Data Engineering*.
2. Harris, C. R., et al. (2020). Array Programming with NumPy. *Nature*.
3. Pedregosa, F., et al. (2011). Scikit-learn: Machine Learning in Python. *Journal of Machine Learning Research*.
