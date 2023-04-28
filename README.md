# OnlineNewsPopularity Data
  
## Summary

In this task, we predict the value of the shares column by pre-processing the data and checking different machine-learning models.

#### Model results with R2_score and training with linear regression without any preprocessing: 0.013436911487878178

#### Model results with R2_score and training with polynomial regression by preprocessing: 0.42482892634462005



## Checking correlation

  <p align="center">
    <img src = "images/cor.png" height = "700" width="1000">
  </p>
    
It can be seen that most of the features are not related to the target.

Therefore, it is not possible to remove a feature easily, because it is possible that some features have a non-linear relationship with the target, and also because the coefficients are very close to each other.

So, removing features in relation to their relationship with the target is not a good thing.


## Checking the distribution of shares

  <p align="center">
    <img src = "images/shear-dis.png" height = "700" width="1000">
  </p>


## Remove outlier records

### IQR :

Due to the deletion of a large part of the data, we abandon this method.

### Z-test :

Due to the non-normality of the distribution, we refrain from using this method.

### Percentile:

By removing one percentage of outlier data :‌

  <p align="center">
    <img src = "images/out.png" height = "700" width="1000">
  </p>

## Scaling

  -  _Quantile Transformer_
  
  <p align="center">
    <img src = "images/Q1.png" height = "350">
  </p>

  - _power transformer_
    <p align="center">
      <img src = "images/p1.png" height = "350">
    </p>
  
  - -min-max-
    <p align="center">
      <img src = "images/min-max1.png" height = "350">
    </p>
    

## Again scaling

Now we rescale the data that we scaled with the Quantile Transformer method


- __**min-mix**__

    <p align="center">
      <img src = "images/min-max2.png" height = "350">
    </p>
    

A very important point is that all data are normally between 0 and 1.

- __**power transformer**__

    <p align="center">
      <img src = "images/p2.png" height = "350">
    </p>
    
- __**RobustScaler**__

    <p align="center">
      <img src = "images/r2.png" height = "350">
    </p>
    
   
    
- __**StandardScaler**__

    <p align="center">
      <img src = "images/r2.png" height = "350">
    </p>
    
    
## using min-max after Quantile


  <p align="center">
    <img src = "images/dis.png" height = "350">
  </p>


## Linear model

R2_score : 0.15420224054686105

## Polynomial model

R2_score : 0.42482892634462005


    
