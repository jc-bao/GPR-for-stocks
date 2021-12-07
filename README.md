# GPR For Stocks Price Prediction

## User Guidance

run `gpr.ipynb` directly.

## Requirements

```
quandl, 
sklearn
```

## Hyperparamters

Note: select the kernel properly is vital to final performance.

 ```
stock_id = 'WIKI/NVDA' # the stock you want to get
input_data_length = 100 # length of input data
predict_data_length = 50 # how many day to predict
# [Important] choice of kernel
kernel = 0.2*RBF(1.5) + 3*RBF(0.3) + WhiteKernel(noise_level=1e-3) + Matern() + RationalQuadratic()*0.1 + ExpSineSquared()*0.2
```