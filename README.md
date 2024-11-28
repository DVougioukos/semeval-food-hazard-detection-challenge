# SemEval Food Hazard Detection Challenge

This repository contains resources and instructions for the second assignment in the Practical Data Science course. The scope of the assignment is to participate in the [Food Hazard Detection Challenge](https://food-hazard-detection-semeval-2025.github.io/ "Link"), where participants analyze provided datasets to identify food hazards. The assignment involves performing benchmark analyses on both short texts ('title' column) and long texts ('text' column) provided by the training dataset using machine learning algorithms and evaluating the results.

## Assignment

The task is to apply and evaluate traditional and advanced machine learning algorithms for the four classification tasks of which the challenge consists, using the provided short and long texts.

**Classification Tasks**
- Detect hazard category
- Detect product category
- Detect hazard vector
- Detect product vector

## Repository Structure

- code
    - data_exploration: A notebook for exploring the provided training dataset
    - classification_benchmark_titles: A notebook for perfoming bechmark analysis using the short texts
    - classification_benchmark_texts: A notebook for perfoming benchmark analysis using the long texts
- data
    - train: Folder containing the training dataset
    - validation: Folder containing the validation dataset
- submission
    - subtask_1: Folder containing the best scoring submission file for the first subtask of the challenge
    - subtask_2: Folder containing the best scoring submission file for the second subtask of the challenge

## Benchmark Analyses Description

For the benchamark analyses on both text types, i select and evaluate 3 machine learning algorithms, which are Logistic Regresion, XGBoost and BERT-RoBERTa model. As you can observe in the included notebooks, in all models i tried as much as i could, considering my computational resources, to adjust the hyperparameters and take into account the extreme class imbalance situation. In each task it is possible to change the training strategy (hyperparameters to tune, etc.) due to the distribution of labels in them and my computational resources, as i mentioned again. 

After evaluating the models for each classification task i used the most robust ones and applied them to the validation dataset provided by the challenge. Below, we present the best models per classification task and based on which feature (short text ('title' column) or long text ('text' column)). Because, the classification tasks are highly unbalanced (as you can observe in the data_exploration notebook), I decided to use the macro f1 metric to evaluate the performance of the algorithms.

In all cells of the notebooks, the code is executed and the results are displayed to easily track the progress of the benchamarks.

- Detect hazard category
    - Algorithm: Logistic Regression
    - Feature: Long text ('text' column)
- Detect product category
    - Algorithm: BERT-RoBERTa
    - Feature: Long text ('text' column)
- Detect hazard
    - Algorithm: Logistic Regression
    - Feature: Long text ('text' column)
- Detect product
    - Algorithm: Logistic Regression
    - Feature: Long text ('text' column)

## Leaderboard - Score - Ranking

Based on my submissions and up to the date of 28-11-2024, i received the following score and ranking in the two subtasks of the challenge:

- Subtask 1
    - Score: 0.7520
    - Rank: 6
- Subtask 2
    - Score: 0.4208
    - Rank: 5