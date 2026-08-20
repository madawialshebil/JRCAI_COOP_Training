# Phase 5 — Model Optimization and Final Evaluation

This phase focused on optimizing the strongest Machine Learning and Deep Learning models selected during Phase 4 and performing the final forecasting comparison.

## Temperature Forecasting Project

Phase 4 identified Random Forest as the strongest classical Machine Learning model and BiLSTM as the strongest Deep Learning model and best overall baseline model.

These two finalist models were carried forward to Phase 5 for hyperparameter optimization and final evaluation.

### Objectives

- Optimize the selected Random Forest and BiLSTM models.
- Compare multiple hyperparameter optimization techniques.
- Evaluate optimization performance using validation RMSE.
- Track and visualize BiLSTM hyperparameter experiments.
- Retrain the selected configurations under consistent final conditions.
- Compare the optimized models and identify the final forecasting model.

### Random Forest Optimization

The Random Forest model was optimized using:

- Manual Tuning
- GridSearchCV
- RandomizedSearchCV

RandomizedSearchCV achieved the strongest validation performance and was selected for final retraining.

### BiLSTM Optimization

The BiLSTM model was optimized using:

- Manual Tuning
- Optuna
- Genetic Algorithm (GA)
- Particle Swarm Optimization (PSO)
- Differential Evolution (DE)
- Simulated Annealing (SA)
- Aquila Optimizer (AO)
- Adaptive Aquila Optimizer (AAO)

The metaheuristic algorithms were implemented using the MEALPY optimization framework.

Optuna was used as a separate automated hyperparameter optimization framework and was extended to 100 total trials.

### Hyperparameters Evaluated

The BiLSTM optimization searched different values for:

- Hidden size
- Number of recurrent layers
- Dropout
- Learning rate
- Batch size
- Weight decay
- Optimizer
- Activation function

### Experiment Tracking and Analysis

TensorBoard HParams was used to visualize and compare BiLSTM hyperparameter experiments.

Optuna parameter importance was also analyzed to estimate which searched hyperparameters had the greatest influence on validation RMSE.

### Evaluation Metrics

- RMSE
- MAE
- R²
- Prediction accuracy within ±1°C

### Key Results

Random Forest optimization reduced test RMSE from **0.5745°C to 0.5674°C**, representing an improvement of approximately **1.24%**.

Among the BiLSTM optimization methods, Optuna achieved the strongest validation performance with an RMSE of **0.5098°C**.

The Optuna study was extended to **100 total trials**, but the additional trials did not further improve the best validation RMSE.

For the final comparison, the baseline and optimized BiLSTM configurations were retrained under the same conditions.

- Retrained Baseline BiLSTM RMSE: **0.5559°C**
- Optimized BiLSTM RMSE: **0.5549°C**
- BiLSTM RMSE improvement: approximately **0.18%**

The **Optimized BiLSTM** achieved the strongest final forecasting performance and was selected as the final model.

## Files

- `Phase5_Model_Optimization.ipynb` — complete Phase 5 model optimization, experiment tracking, final retraining, and evaluation.
- `Phase5_Model_Optimization.py` — Python version of the Phase 5 workflow.
- `Final_Presentation.pdf` — final presentation covering the complete Temperature Forecasting Project across Phase 4 and Phase 5.
