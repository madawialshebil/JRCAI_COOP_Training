# SDAIA-KFUPM JRCAI COOP Training

This repository documents the assignments, reports, notebooks, and projects completed during my COOP training.

## Repository Structure

### Phase 1: Research Foundations

This phase focuses on research skills, Python programming, and data science fundamentals.

### Phase 2: Machine Learning Foundations

This phase focuses on data preparation, machine learning techniques, model development, and evaluation.

### Phase 3: Deep Learning with PyTorch

This phase focuses on PyTorch fundamentals, deep learning workflows, model training, and evaluation.

### Phase 4: AI Domains and Advanced Deep Learning

This phase focuses on applying advanced Machine Learning and Deep Learning techniques to sequential and time-series data.

The main project in this phase was a temperature forecasting system using the Jena Climate dataset. Multiple classical Machine Learning and recurrent Deep Learning models were developed and compared, including Linear Regression, Random Forest, XGBoost, RNN, LSTM, GRU, and BiLSTM.

Random Forest achieved the strongest performance among the classical Machine Learning models, while BiLSTM achieved the strongest Deep Learning performance and the best overall baseline forecasting result.

### Phase 5: Model Optimization and Final Evaluation

This phase focuses on hyperparameter optimization and final evaluation of the strongest models selected during Phase 4.

Random Forest was optimized using Manual Tuning, GridSearchCV, and RandomizedSearchCV.

BiLSTM was optimized using Manual Tuning, Optuna, and several metaheuristic optimization algorithms implemented through MEALPY, including GA, PSO, DE, SA, AO, and AAO.

TensorBoard HParams was also used to track and visualize BiLSTM hyperparameter experiments, and Optuna parameter importance was analyzed.

The final optimized BiLSTM achieved the strongest overall forecasting performance and was selected as the final model for one-hour-ahead temperature forecasting.

The combined Phase 4 and Phase 5 presentation is included in the Phase 5 folder.
