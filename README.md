# Algorithmic Trading Strategy Optimization

This repository contains a machine learning-based project focused on tuning a trading algorithm and comparing different models' performance. The goal of this project is to design a better trading algorithm and evaluate its performance.

## Content
The repository is composed of Jupyter notebooks, datasets, and resulting plots. Here's what each file/section does:

- The main Jupyter notebook contains the code for the machine learning models and trading algorithms.
- The 'Resources' folder contains saved plots showing the performance of various trading algorithms.

## Project Tasks

This project consists of four main tasks:

### 1. Establish a Baseline Performance
Firstly, a simple moving average crossover (SMA) trading strategy is implemented using the SVC classifier from sklearn's support vector machine (SVM) learning method. The performance of this trading algorithm serves as our baseline. A cumulative return plot was generated to visualize the performance of the algorithm:

![Cumulative Returns Plot 1](./Resources/cumulative_returns_plot1.png)

### 2. Tune the Baseline Trading Algorithm
To enhance the baseline algorithm's performance, the following steps were carried out:

- **Tuning the Training Algorithm**: The size of the training dataset was adjusted. The data was sliced into different periods and the notebook was rerun with the updated parameters. The performance of the algorithm improved, as the strategy returns increased from 1.5 to 1.6 and the actual returns from 1.4 to 1.5.

Initially, the ending period for the training data was set with an offset of 3 months and the short and long windows for the SMA were set to 4 and 100 respectively.

```python```
# Select the ending period for the training data with an offset of 3 months
training_end = X.index.min() + DateOffset(months=3)

# Set the short window and long window
short_window = 4
long_window = 100

After adjustment, the ending period for the training data was set with an offset of 5 months and the short and long windows for the SMA were set to 2 and 60 respectively.

# Select the ending period for the training data with an offset of 5 months
training_end = X.index.min() + DateOffset(months=5)

# Set the short window and long window
short_window = 2
long_window = 60

- **Tuning the Training Algorithm**: The windows for the SMA algorithm were adjusted and the notebook was rerun with the updated parameters. This resulted in better performance of the trading algorithm.

After tuning, the set of parameters that best improved the trading algorithm returns was selected and a new cumulative return plot was generated:

![Cumulative Returns Plot 2](./Resources/cumulative_returns_plot2.png)

### 3. Evaluate a New Machine Learning Classifier
A new classifier, AdaBoost, DecisionTreeClassifier, or LogisticRegression will be used to fit the model. The performance of this new model will be backtested and compared with the baseline model.

### 4. Create an Evaluation Report
Finally, an evaluation report will be created summarizing the final conclusions and analysis. This report will be supported by the PNG images created throughout the project.

## Conclusion 
This project is ongoing and the README will be updated with the conclusions once all the tasks are completed.

**Please note**: This project is an academic exercise and is not intended to be a guide for real-world trading. The algorithms and strategies used in this project may not be suitable for actual trading and are not recommended for use in live trading without further enhancements and testing.




