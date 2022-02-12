## MechaCar_Statistical_Analysis

<img width="747" alt="Screen Shot 2022-02-12 at 5 05 01 PM" src="https://user-images.githubusercontent.com/90429568/153729958-c5908da8-c159-49fe-8a3e-4832f309934a.png">

From the output above, it can be noted that the vehicle length and ground clearance provide non-random amounts of variance in the model. In fact, it is important to note that length and clearnace have significant impact on miles per gallon the Mecha-Car prototype. On the other hand, weight, angle and all wheel drive (AWD) have p-values that indicate random amount of variance with the dataset. 

Since the p-value of this model 5.35e-11, which is much lower than 0.05%, it can be concluded that the sole of this model is not zero. 

Since the r-value is 0.7149, indicating that 71% of all mpg predictions can be determined by this model, making this model very effective to predict mpg of MechaCar prototypes. The predictablity measure does take a blow slightly when the less impactful variables such as vehicle weight, spoiler angle, and all wheel drive are removed from the model, the r-value drops from 0.7149 to 0.674. Since, the drop is not huge, the model is still effective in predicting the mpg of MechaCar prototypes. As demonstrated in the output below. 


<img width="816" alt="Screen Shot 2022-02-12 at 5 56 49 PM" src="https://user-images.githubusercontent.com/90429568/153731437-63b8abf0-10b4-4d91-bb2c-ba839c95e4a1.png">

## Summary Statistics on Suspension Coils

<img width="816" alt="Screen Shot 2022-02-12 at 5 58 43 PM" src="https://user-images.githubusercontent.com/90429568/153731474-b6eaca0d-73f1-4dd8-ba8b-2aee57936c7a.png">

From the above summary table, it can be noted that the variance of coils is 62.29 PSI, this number is well-under the 100 psi, as such the current manufacturing data meet this design specification for all manufacturing lots in total.

However, to examine if the manufacturing data meets the design specification in each lot, lot summary table (displayed below) should be analyzed.

<img width="690" alt="Screen Shot 2022-02-12 at 6 02 53 PM" src="https://user-images.githubusercontent.com/90429568/153731584-26d79438-0bec-4eab-ae49-1d54d7107613.png">

From this output, it is clearly visible that lot 1 and lot 2 are well within the 100 PSI variance requirement; with variances of 0.98 and 7.47 respectively. However, Lot 3 shows larger variance in performance and consistency, with a variance of 170.29, as such Lot 3 is disproportionately causing the variance at the full lot level.

## T-Tests on Suspension Coils

Summary of the t-test results across all manufacturing lots

<img width="439" alt="Screen Shot 2022-02-12 at 6 14 16 PM" src="https://user-images.githubusercontent.com/90429568/153731820-923a7fcf-cb29-4816-9af0-071768b18af7.png">

This output summarizes the mean output of the sample: 1498.78. Since the p-value is 0.06, higher than 0.05, this indicates there is not enough evidence to reject the null hypothesis. As such the mean of the thre manufacturing lots is statistically similar to population mean of 1500. 

Individual lots:

<img width="779" alt="Screen Shot 2022-02-12 at 6 17 03 PM" src="https://user-images.githubusercontent.com/90429568/153731883-26772ffd-c12f-4bc5-9c73-a081c2468bf8.png">

<img width="668" alt="Screen Shot 2022-02-12 at 6 17 20 PM" src="https://user-images.githubusercontent.com/90429568/153731891-2f122a69-d922-4e19-bf74-6fd743c561a0.png">

Lot 1 sample has the same mean value as the population=1500. p-value is 1, higher than 0.05 and as such null hypothesis cannot be rejected and it can be concluded that there is no statistically significant difference between the observed mean and population mean.

Similarly, lot 2 has similar sample mean of 1500.2 in comparison to the population mean of 1500. p-value 0.6072, higher than 0.05, indicative that there is no statistically significant difference between the observed mean of lot 2 and population mean (i.e. accept the null hypothesis).

On the other hand lot 3 is significantly different from the population mean as the observed mean in this case is 1496 with a p-value of 0.041. Since the p-value is less than 0.05, we reject the null hypothesis; thereby indicating that there is a statistically significant difference between the observed mean and population mean. 

## Study Design: MechaCar vs Competition

A study comparing the MechaCar to comparable models for offroad capabilities. Metrics to measure would include: 
1. Price of the car: Dependent variable
2. Drivetrain of the car (AWD vs 4WD vs FWD vs RWD): Independent variable
3. Engine (Gasoline/Diesel/Electric/Hybrid): Independent variable
4. Tires included in base model: Independent variable
5. Ground clearance: Independent variable
6. Performance on an offroad track: Dependant variable

Null Hypothesis: MechaCar performs as well as/better offroad than other car models with the same comparable specifications. 
Alternative hypothesis: MechaCar performs worse than other car models offroad with the same comparable specifications.

Multiple linear regression model will be used to see which factors from the independent variable have the most effect on the offroad performance of the MechaCar, as well as the the required price of the car with those specifications. 
