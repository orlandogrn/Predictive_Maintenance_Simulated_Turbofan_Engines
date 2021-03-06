# Predictive Maintenance Project: Simulated Turbofan Engines Data

## Project overview
Predictive maintenance aims to increase system reliability and be more cost efficient than time-based only preventive maintenance. This project focused on estimating the “remaining useful life (RUL)” of a machine, more specifically in this case of aircraft turbofan engines whose dataset used was from a NASA competition where simulated turbofan engines signals were provided.

Several machine learning models (Elastic Net, Random Forest, Gradient Boosting, Logistic Regression, SVM, Neural Network, among others) were tuned and compared to predict a failure occurrence. Results were improved by using feature engineering (moving average window), feature normalisation by operating regime and modelling gridsearch. Neural Network, Gradient Boosting and SVR models showed the best performances.

This was an individual project was developed during the Data Science course at General Assembly London.

## Data

The data used in this project was made available by NASA:

Turbofan Engine Degradation Simulation Data Set (https://ti.arc.nasa.gov/tech/dash/groups/pcoe/prognostic-data-repository/#turbofan).

It is a multivariate time series and includes a total of 26 channels:
- an number ID for each turbofan engine.
- the operating 'cycle' as the time unit.
- three operating settings (altitude, mach and throttle resolver angle(TRA)).
- 21 sensor readings, which are described on Table 1 below.


<p align="center">
	Table:1 Channels description
</p>
<p align="center">
	<img src="ReadMe_files/channels_description.png" height="650" width="425" />
</p>

There are a total of four simulated datasets available on the NASA data repository website. Each dataset contains a different number of fault modes, operating conditions (different altitude, mach and TRA combinations), and number of engines as shown on Table 2.

<p align="center">
	Table:2 Datasets avaiblable at NASA website
</p>
<p align="center">
	<img src="ReadMe_files/datasets_table.png" height="240" width="500" />
</p>

## Summary
- The use of the operating conditions and the creation of new features (based on the operating regimes and sensors readings) was crucial to improve prediction performance.
- The progressive increase of engine wear is a key characteristic to predict failure, and so models that take a form of “wear” into account seem to perform better.
- MLP, Gradient Boosting and SVR have shown to be the best performers among the models tried.

## Potential future work
- To analyse the models performance varying the initial RUL.
- To apply component analysis to select features.
- To Assess the performance of other models that keep some memory of past events such as LSTM and others.
- Use of classification models to predict whether or not a failure may occur in a time window.
- Use of classification to identify possibly different failure modes.
