Feature Engineering Steps for Bank Marketing Dataset

1. Data Cleaning & Preparation
    Target Conversion: The target variable y was converted from text ('yes', 'no') to a numerical binary format (1 and 0).

    Missing Value Imputation:

        Textual missing values ('unknown') were replaced with NaN.

        Numerical features (e.g., age) were imputed using the median.

        Categorical features (e.g., job) were imputed using the mode (most frequent value).

2. Encoding & Scaling
    One-Hot Encoding: All categorical features were converted into multiple binary columns (e.g., job became job_admin., job_blue-collar, etc.) to make them usable by algorithms.

    Feature Scaling: Standard Scaling was applied to all numerical features to normalize their range, ensuring a mean of 0 and a standard deviation of 1. This prevents features with larger magnitudes (like duration) from unfairly dominating the model

3. Feature Optimization
    PCA (Dimensionality Reduction): Principal Component Analysis was used to reduce the high-dimensional feature set to 2 components (PC1, PC2) for structure analysis and visualization.

    SelectKBest Selection: The top 8 most statistically predictive features were selected using the ANOVA F-value (f_classif). This reduces noise and improves model efficiency and performance.