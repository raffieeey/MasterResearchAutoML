# Automated Machine Learning : The Study of Top Algorithm Based On Benchmark Dataset


- [x] H2O AutoML
- [x] TPOT
- [x] Auto-sklearn
- [ ] Hyperopt-Sklearn #Only Classifier, No Regression

# Related papers          
- (1) Hyperopt-Sklearn (Komer et al., 2014): https://github.com/openml/automlbenchmark/tree/master/frameworks
- (2) Auto-sklearn (Feurer et al., 2019): https://github.com/openml/automlbenchmark/tree/master/frameworks
- (3) Auto-Net (Mendoza et al., 2019): https://github.com/automl/Auto-PyTorch
- (4) H2O’s AutoML (H2O.ai, 2017): https://github.com/openml/automlbenchmark/tree/master/frameworks
- (5) TPOT (Olson et al., 2016): https://github.com/openml/automlbenchmark/tree/master/frameworks

# datasets
## class 
- adult --https://www.openml.org/d/1590
- agaricus-lepiota --https://www.openml.org/d/24
- churn --https://www.openml.org/d/40701
- nursery --https://www.openml.org/d/1568
- satimage --https://www.openml.org/d/182
- texture --https://www.openml.org/d/40499


## regression
- 294_satellite_image --https://www.openml.org/d/294
- 218_house_8L --https://www.openml.org/d/218
- 227_cpu_small --https://www.openml.org/d/562
- 503_wind --https://www.openml.org/d/503
- 344_mv --https://www.openml.org/d/344
- 215_2dplanes --https://www.openml.org/d/215

## Script for selected dataset
```python
sel_clss_dtst = ['adult','agaricus-lepiota', 'churn', 'nursery', 'satimage','texture']
sel_rgrs_dtst = ['294_satellite_image','218_house_8L', '227_cpu_small', '503_wind', '344_mv','215_2dplanes']
```

## Loop dataset
```python
for regrs_dtst in sel_rgrs_dtst:
    df = fetch_data(regrs_dtst)
    print("Dataframe Name: ",regrs_dtst, ", Dataframe size: ", df.shape)
    
for class_dtst in sel_clss_dtst:
    df = fetch_data(class_dtst)
    print("Datasets Name: ",class_dtst, " , Number of missing values : ", df.isnull().sum().sum())
```

## AUCpr
AUCPR = http://pages.cs.wisc.edu/~jdavis/davisgoadrichcamera2.pdf

© 2019 GitHub, Inc.
