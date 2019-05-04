# Preston Baker MAE 301 Project
### Executive Summary

### Introduction
  In this project I will be testing the accuracy of a car’s “miles to empty” display. Many cars have a number that will tell you how many miles you can drive until you are out of gas. This number is meant to be a close estimate, so I will be testing if it can be trusted. How many miles per gallon a car gets each time it is driven is affected by air temperature, terrain, aggressiveness of driving, added weight such as a trailer, and even using of air conditioning (www.fueleconomy.gov). Thus, every test would not be expected to be exactly as the display predicted. However, it would be expected that on average it is a close estimate and can be assumed true. My null hypothesis is that I will find the distance travelled according to the MTE (miles to empty) display is equal to the distance travelled according to the car's odometer, inferring that all factors affecting fuel consumption are negligible.

  I will test my null hypothesis by taking multiple samples with my car. Each sample will start when I fill up my car with gas. I will log the numbers displayed by my odometer and by the miles to empty display. I will then drive as I normally do and not take into account any of the factors affecting fuel consumption. Once I return to the gas station as normal, I will fill it up again after first writing down what my MTE display now reads. Noting the odometer I can see how far I travelled since my last stop at the gas station. The distance travelled according to the odometer should match the change in distance reported by the MTE reading. Once I collect as many samples as I can in my predetermined time frame, I will use my compiled data to find my sample means and sample variances. Since I cannot confirm that the reading by the odometer is correct either, I will take that as a second group of samples. Using these sample means and sample variances I will perform a two sample t test without assuming the variances are equal to see if the null hypothesis can be rejected. I will find a confidence interval in a yet to be determined range as well.

### Procedures and Results
Car Fueling Data

Starting odometer reading: 81237

Initial measurements acquired:

| Trial | Miles to E Start | Miles to E End | Odometer Reading |
| --- | --- | --- | --- |
| 1 | 366 | 8 | 81567 |
| 2 | 362 | 34 | 81901 |
| 3 | 352 | 45 | 82222 | 
| 4 | 360 | 22 | 82550 | 



To test the hypothesis I need to acquire from this the predicted distance travelled and the distance travelled according to the odometer

| Trial | MTE distance | Odometer distance |
| --- | --- | --- |
| 1 | 366-8=358 | 81567-81237=330 |
| 2 | 362-34=328 | 81901-81567=334 |
| 3 | 352-45=307 | 82222-81901=321 |
| 4 | 360-22=338 | 82550-82222=328 |

Using this data I can calcuate my two sample means and sample variances.

![equation](https://latex.codecogs.com/gif.latex?%5Coverline%7Bx_%7B1%7D%7D%3D%5Cfrac%7B358&plus;328&plus;307&plus;338%7D%7B4%7D%3D332.75)

![equation](https://latex.codecogs.com/gif.latex?%5Coverline%7Bx_%7B2%7D%7D%3D%5Cfrac%7B330&plus;334&plus;321&plus;328%7D%7B4%7D%3D328.25)

![equation](https://latex.codecogs.com/gif.latex?s_%7B1%7D%5E%7B2%7D%3D%5Cfrac%7B%28%28358-332.75%29%5E%7B2%7D&plus;%28328-332.75%29%5E%7B2%7D&plus;%28307-332.75%29%5E%7B2%7D&plus;%28338-332.75%29%5E%7B2%7D%29%7D%7B3%7D%3D450.25)

![equation](https://latex.codecogs.com/gif.latex?s_%7B2%7D%5E%7B2%7D%3D%5Cfrac%7B%28%28330-328.25%29%5E%7B2%7D&plus;%28334-328.25%29%5E%7B2%7D&plus;%28321-328.25%29%5E%7B2%7D&plus;%28328-328.25%29%5E%7B2%7D%29%7D%7B3%7D%3D28.5833)

I now have all of the information I need to find the T value

![equation](https://latex.codecogs.com/gif.latex?T%3D%5Cfrac%7B%28%5Coverline%7Bx_%7B1%7D%7D-%5Coverline%7Bx_%7B2%7D%7D%29-%28%5Cmu_1-%5Cmu_2%29%7D%7B%5Csqrt%7Bs_%7B1%7D%5E%7B2%7D/n_1&plus;s_%7B2%7D%5E%7B2%7D/n_2%7D%7D)

I am testing whether the population means equal each other, so the equation becomes

![equation](https://latex.codecogs.com/gif.latex?T%3D%5Cfrac%7B%28%5Coverline%7Bx_%7B1%7D%7D-%5Coverline%7Bx_%7B2%7D%7D%29%7D%7B%5Csqrt%7Bs_%7B1%7D%5E%7B2%7D/n_1&plus;s_%7B2%7D%5E%7B2%7D/n_2%7D%7D)

Thus

![equation](https://latex.codecogs.com/gif.latex?T%3D%5Cfrac%7B%28332.75-328.25%29%7D%7B%5Csqrt%7B%5Cfrac%7B450.25%7D%7B4%7D&plus;%5Cfrac%7B28.5833%7D%7B4%7D%7D%7D%3D.41129)

The formula for degree of freedom is 

![equation](https://latex.codecogs.com/gif.latex?%5Cfrac%7B%28%5Cfrac%7Bs_%7B1%7D%5E%7B2%7D%7D%7Bn_1%7D&plus;%5Cfrac%7Bs_%7B2%7D%5E%7B2%7D%7D%7Bn_2%7D%29%5E%7B2%7D%7D%7B%5Cfrac%7B%28%5Cfrac%7Bs_%7B1%7D%5E%7B2%7D%7D%7Bn_1%7D%29%5E%7B2%7D%7D%7Bn_%7B1%7D-1%7D&plus;%5Cfrac%7B%28%5Cfrac%7Bs_%7B2%7D%5E%7B2%7D%7D%7Bn_2%7D%29%5E%7B2%7D%7D%7Bn_%7B2%7D-1%7D%7D)

Thus

![equation](https://latex.codecogs.com/gif.latex?dof%3D%5Cfrac%7B%28%5Cfrac%7B450.25%7D%7B4%7D&plus;%5Cfrac%7B28.5833%7D%7B4%7D%29%5E%7B2%7D%7D%7B%5Cfrac%7B%28%5Cfrac%7B450.25%7D%7B4%7D%29%5E%7B2%7D%7D%7B3%7D&plus;%5Cfrac%7B%28%5Cfrac%7B28.5833%7D%7B4%7D%29%5E%7B2%7D%7D%7B3%7D%7D%3D%5B3.38%5D%3D3)

I will use ![equation](https://latex.codecogs.com/gif.latex?%5Calpha) = 0.05, as is typically standard, meaning I have 95% confidence that my conclusion in regards to the null hypothesis will be accurate.

The following lines are coded into python to find both the T score and the p-value:

```
from scipy.stats import t
print(t.ppf(.025, 3))
print(t.ppf(.975, 3))
```

This yields -3.1824 and 3.1824

```
T = .41129  # input the value of t-statistic already found along with the degree of freedom
dof = 3  # degree of freedom 
p = 1 - t.cdf(T,df=dof)  # p-value
print(p)
```

This yields 0.3542
