# Preston Baker MAE 301 Project
### Executive Summary

### Introduction
  In this project I will be testing the accuracy of a car’s “miles to empty” display. Many cars have a number that will tell you how many miles you can drive until you are out of gas. I assume this number is meant to be a close estimate, so I will be testing if it can be trusted. Many factors affect gas consumption, such as road conditions, outside temperature, and pressure of tires. Thus, every test would not be expected to be exactly as the display predicted. However, it would be expected that on average it is a close estimate and can be assumed true. My null hypothesis is that I will find the distance travelled according to the MTE (miles to empty) display is equal to the distance travelled according to the car's odometer.

  I will test my null hypothesis by taking as many samples as I can with my car. Each sample will start when I fill up my car with gas. I will log the numbers displayed by my odometer and by the miles to empty display. I will then drive as I normally do and not take into account any of the factors I mentioned earlier, such as road conditions. Once I return to the gas station due to my tank being near empty, I will fill it up again after first writing down what my MTE display now reads. Noting the odometer I can see how far I travelled since my last stop at the gas station. The distance travelled according to the odometer should match the change in distance reported by the MTE reading. I will perform samples up until the end of the project. With my data compiled I can find my sample means and sample variances. Since I cannot confirm that the reading by the odometer is correct, I will take that as a second group of sampling. Using these sample means and sample variances I will perform a two sample t test without assuming the variances are equal to see if the null hypothesis can be rejected. I will find a confidence interval in a yet to be determined range as well.

### Procedures and Results
Car Fueling Data
Starting odometer reading: 81237
Initial measurements acquired:

| Trial | Miles to E Start | Miles to E End | Odometer Reading |
| --- | --- | --- | --- |
| 1 | 366 | 8 | 81567 |
| 2 | 362 | 34 | 81901 |
| 3 | 352 | - | - | 
| 4 | - | - | - | 



To test the hypothesis I need to acquire from this the predicted distance travelled and the distance travelled according to the odometer

| Trial | MTE distance | Odometer distance |
| --- | --- | --- |
| 1 | 366-8=358 | 81567-81237=330 |
| 2 | 362-34=328 | 81901-81567=334 |
| 3 | - | - |
| 4 | - | - |
Using this data I can calcuate my two sample means and sample variances.

![equation](https://latex.codecogs.com/gif.latex?%5Coverline%7Bx_1%7D%3D%5Cfrac%7B358&plus;328&plus;n3%7D%7B3%7D%3D)

![equation](https://latex.codecogs.com/gif.latex?%5Coverline%7Bx_2%7D%3D%5Cfrac%7B330&plus;334&plus;n3%7D%7B3%7D%3D)

LaTeX codes are \overline{x_{1}}=\frac{358+328+n3+n4}{4} for mean and s_{1}^{2}=\frac{1}{4-1}\cdot {((358-\overline{x}))+((328-xbar))} for variance 

I now have all of the information I need to find the T value

![first eq](https://latex.codecogs.com/gif.latex?T%3D%5Cfrac%7B%28%5Coverline%7Bx_%7B1%7D%7D-%5Coverline%7Bx_%7B2%7D%7D%29-%28%5Cmu_1-%5Cmu_2%29%7D%7B%5Csqrt%7Bs_%7B1%7D%5E%7B2%7D/n_1&plus;s_%7B2%7D%5E%7B2%7D/n_2%7D%7D)

I am testing whether the population means equal each other, so the equation becomes

![second eq](https://latex.codecogs.com/gif.latex?T%3D%5Cfrac%7B%28%5Coverline%7Bx_%7B1%7D%7D-%5Coverline%7Bx_%7B2%7D%7D%29%7D%7B%5Csqrt%7Bs_%7B1%7D%5E%7B2%7D/n_1&plus;s_%7B2%7D%5E%7B2%7D/n_2%7D%7D)

The formula for degree of freedom is 

![equation](https://latex.codecogs.com/gif.latex?%5Cfrac%7B%28%5Cfrac%7Bs_%7B1%7D%5E%7B2%7D%7D%7Bn_1%7D&plus;%5Cfrac%7Bs_%7B2%7D%5E%7B2%7D%7D%7Bn_2%7D%29%5E%7B2%7D%7D%7B%5Cfrac%7B%28%5Cfrac%7Bs_%7B1%7D%5E%7B2%7D%7D%7Bn_1%7D%29%5E%7B2%7D%7D%7Bn_%7B1%7D-1%7D&plus;%5Cfrac%7B%28%5Cfrac%7Bs_%7B2%7D%5E%7B2%7D%7D%7Bn_2%7D%29%5E%7B2%7D%7D%7Bn_%7B2%7D-1%7D%7D)

Thus

![equation](https://latex.codecogs.com/gif.latex?%5Cfrac%7B%28%5Cfrac%7Bs_%7B1%7D%5E%7B2%7D%7D%7Bn_1%7D&plus;%5Cfrac%7Bs_%7B2%7D%5E%7B2%7D%7D%7Bn_2%7D%29%5E%7B2%7D%7D%7B%5Cfrac%7B%28%5Cfrac%7Bs_%7B1%7D%5E%7B2%7D%7D%7Bn_1%7D%29%5E%7B2%7D%7D%7Bn_%7B1%7D-1%7D&plus;%5Cfrac%7B%28%5Cfrac%7Bs_%7B2%7D%5E%7B2%7D%7D%7Bn_2%7D%29%5E%7B2%7D%7D%7Bn_%7B2%7D-1%7D%7D)


code for dof is \frac{(\frac{s_{1}^{2}}{n_1}+\frac{s_{2}^{2}}{n_2})^{2}}{\frac{(\frac{s_{1}^{2}}{n_1})^{2}}{n_{1}-1}+\frac{(\frac{s_{2}^{2}}{n_2})^{2}}{n_{2}-1}}
