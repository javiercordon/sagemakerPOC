# sagemaker-POC
Sagemaker Proof of Concept without extra feature engineering in data input

## Background
Getting customized models may be time consuming compared to auto ML or auto Tunning available from Cloud providers as AWS. We would like to have as a reference what could be te minimum accuracy target we could get when designing a customized model.

## Description
This project has 3 different notebooks to address LinearModel specific accuracy target training, XGBoost Hyper Parameter auto Tunning, and AutoPilot.

## Usage
Run each of the 3 main jupyter notebooks downloading dataset. In this case data has been previously clean from empty values, and categories turned into a number.

## Results

|    | Sagemaker                                 | TPR   | TNR   | Recall   | Precision   | Accuracy   |
|---:|:------------------------------------------|:------|:------|:---------|:------------|:-----------|
|  0 | Linear                                    | 15.9% | 95.7% | 15.9%    | 56.7%       | 74.6%      |
|  1 | Linear (target recall  0.60)              | 58.9% | 71.0% | 58.9%    | 42.2%       | 67.8%      |
|  2 | Linear (target recall - balanced 0.58)    | 56.6% | 73.0% | 56.6%    | 42.9%       | 68.7%      |
|  3 | Linear (target precision - balanced 0.60) | 8.4%  | 97.9% | 8.4%     | 58.7%       | 74.3%      |
|  4 | XGB (HP Tunning 50 models)                | 33.5% | 94.6% | 33.5%    | 67.8%       | 79.2%      |
|  5 | AutoML (AutoPilot)                        | 42.0% | 89.5% | 42.0%    | 57.7%       | 77.4%      |
