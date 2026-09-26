Dubai Real Estate Analytics
This project applies supervised and unsupervised machine learning techniques to Dubai real estate transaction data, covering regression, classification, and clustering tasks. Using a cleaned dataset of over 350,000 sales transactions, the notebooks explore how structural, locational, and temporal attributes drive property pricing. Regression models (Linear Regression vs. Random Forest) predict log-transformed sale prices, classification models (Decision Tree vs. Logistic Regression) segment transactions into Low, Medium, and High price tiers, and K-Means clustering identifies homogeneous residential property segments without using price information. Tree-based models consistently outperform linear baselines, confirming that real estate pricing exhibits nonlinear and interaction-based patterns. SHAP and feature importance analyses highlight procedure_area as the dominant pricing driver across all tasks.

Highlights
Regression (RegressionP.ipynb): Compares Linear Regression and Random Forest for predicting log-transformed sale prices; Random Forest reduces MAE by ~48% and RMSE by ~33%, achieving R² ≈ 0.89.

Classification (ClassificationP.ipynb): Classifies sales into Low / Medium / High price tiers using Decision Tree and Logistic Regression; Decision Tree achieves ~88% accuracy vs. ~81% for Logistic Regression, with notably stronger recall on the minority High tier.

Clustering (KMP.ipynb): Applies K-Means (k=4) to residential Units and Villas, revealing four structurally distinct segments driven primarily by property size, room count, property type, and parking availability.

Feature Engineering: Extracts transaction year/month, parses rooms_en into numeric room counts (with Studio → 0), and encodes property type and location attributes.

Interpretability: Uses impurity-based feature importance, linear coefficient magnitudes, and SHAP values to identify key pricing drivers — property area, transaction year, and premium locations (e.g., Burj Khalifa, Palm Jumeirah).

Model Validation: Employs stratified train/test splits and 5-fold cross-validation to confirm stability and generalization across all models.

Consistent Finding: Property size (procedure_area) is the single most influential predictor across regression, classification, and clustering tasks.

