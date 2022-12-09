# MLReproducibilityChallenge22_TS2Vec
## Reproduction code for 22 ML Reproducibility Challenge

## Scope of reproducibility
We evaluate the reproducibility of the paper _TS2Vec: Towards Universal Representation of Time Series_ by Yue et. al., in order to verify their main claims, which state (i) TS2Vec outperforms SOTAs on benchmark time series tasks, specifically, classification and forecasting, and (ii) their proposed framework, TS2Vec, can learn contextual representations of time series data for arbitrary sub-series at various semantic levels, which is useful for accomplishing the aforementioned benchmark tasks.

## Methodology
Using the published TS2Vec codebase [yuezhihan/ts2vec](https://github.com/yuezhihan/ts2vec) and referenced time series datasets, we reproduced most of the forecasting (univariate and multivariate) and a portion of the classification results presented in the paper. We then investigated the performance of TS2Vec on forecasting a new time series measuring groundwater level in a rain garden. We conducted a hyperparameter search and modified the source code to make the forecasting results visualizable. Our reproducibility study comes at a total computational cost of 3.163 GPU hours.

## Results
We confirmed claim (i), by reproducing the reported accuracy of univariate forecasting, multivariate forecasting, and classification to within -2.39\%, -3.77\%, and -0.56\% of the reported values, supporting the claim that TS2Vec outperforms existing SOTAs. Our investigation into claim (ii), centered around showing TS2Vec's transferability for forecasting the new dataset, has yielded poor results. We have found that in spite of reporting good metrics, TS2Vec may have previously unidentified limitations. 

## What was easy
The original code implementation was publicly accessible and well structured. Replicating the experiments reported in the paper was straightforward. 

## What was difficult
Minimal sample code is provided to support applying the algorithm to other datasets. Successfully training a model and then visualizing forecasting on a new dataset was nontrivial. Script arguments were built out to enable modification of some hyperparameters, but not all. We had to edit the source code to complete our investigation and visualize our results. 

## Communication with original authors
We requested and received the appendix from the corresponding author. We also requested the code for reproducing the plots in the manuscript but did not get a response.
