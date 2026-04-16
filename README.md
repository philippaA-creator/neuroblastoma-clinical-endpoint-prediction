# neuroblastoma-clinical-endpoint-prediction
Machine learning models for clinical endpoint prediction in neuroblastoma using RNA-seq gene expression data from 498 primary tumour samples.

# Background
Neuroblastoma is a paediatric cancer with highly variable outcomes. This project evaluates the capability of RNA-seq-based gene expression profiles to predict clinical endpoints including high-risk classification, disease progression, and survival, using data from 498 primary tumour samples.
Data source: Kocak et al. — RNA-Seq reveals an unprecedented complexity of the neuroblastoma transcriptome and is suitable for clinical endpoint prediction.
Methods
<img width="1278" height="719" alt="image" src="https://github.com/user-attachments/assets/7bf8aa25-334d-4a3d-a0db-2dc64d39c40a" />

# Data: 
log2 FPKM gene expression matrix (RNA-seq), 498 neuroblastoma samples split into training and validation sets
Target variable: High-risk classification (primary focus), with additional endpoints including progression and death from disease
# Models evaluated: 
Neural network, SVM, Random Forest, k-NN
# Validation: 
Stratified k-fold cross-validation, GridSearchCV for hyperparameter tuning
# Neural network architecture: 
Two hidden layers, ReLU activation, Adam optimiser, L2 regularisation, early stopping

Key Results

Best model: Neural network with ROC-AUC of 0.981 on high-risk classification
Regularisation (L2 + early stopping) was critical for managing overfitting in this high-dimensional setting
Comparative analysis showed neural networks outperformed SVM, Random Forest, and k-NN on high-risk endpoint
