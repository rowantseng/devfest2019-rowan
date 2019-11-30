# GDG DevFest Taipei 2019 - 用 BigQuery 帶你快速完成第一個ML專案

## Main Tasks
![mlsteps](images/mlsteps.png?raw=true "mlsteps")
This session demonstrates how a data scientist deals with machine learning tasks using common standard techniques, or Google serverless service, BigQuery. 

### Task 1
The prediction task is to determine whether a person makes over 50K a year. How I build the machine learning model is followed by the 5 steps above. First, `census.ipynb` loads data from google drive and then preprocess(max-min normalization for numeric columns and one-hot encoding for categorical columns). In the meanwhile, visualization helps explore data insights from digits. Finally, I use `RandomForestClassifier` for building a classification model(accuracy=0.85). Others metrics please refer below.
```
        precision    recall    f1-score    support
<=50K      0.82       0.49        0.61       1960
>50K       0.86       0.97        0.91       6181
```
### Task 2
The prediction task is to regress the current rain levels in Taiwan. `weather.ipynb` also follows the common processes as mentioned in task 1. `RandomForestRegressor` is choosed for the regression task.
```
MSE: 0.1360667400933136
MAE: 0.08636690861864049
```

## Datasets
- Task 1: Kaggle 人口普查資料
- Task 2: 氣象資料開放平臺雨量觀測資料

## Bibtex
```
@misc{Dua:2019 ,
    author = "Dua, Dheeru and Graff, Casey",
    year = "2017",
    title = "{UCI} Machine Learning Repository",
    url = "http://archive.ics.uci.edu/ml",
    institution = "University of California, Irvine, School of Information and Computer Sciences" }
```

## License
政府資料開放授權條款第1版

## Links
https://www.kaggle.com/jyotsnaparyani/adult-census-data
https://opendata.cwb.gov.tw/dataset/observation/O-A0002-001
