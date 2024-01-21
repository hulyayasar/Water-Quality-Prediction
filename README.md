# Water Potability Prediction

## Introduction
The goal of this project is to perform exploratory data analysis (EDA), prepare the data for modelling, train and evaluate the data through various machine learning models, and present the results.
We have chosen a dataset from Kaggle which predicts water potability using various water quality attributes.
Original Dataset Source: Kadiwal, Aditya. (2020). Water Quality. Kaggle. https://www.kaggle.com/datasets/adityakadiwal/water-potability.

## Water Quality Dataset Description
### Attributes for dataset:
_1. pHvalue:_ PH is an important parameter in evaluating the acid–base balance of water.It is also the indicator of acidic or alkaline condition of water status. WHO has recommended maximum permissible limit of pH from 6.5 to 8.5. The current investigation ranges were 6.52–6.83 which are in the range of WHO standards.<br><br>
2. Hardness:Hardnessismainlycausedbycalciumandmagnesiumsalts.Thesesaltsare dissolved from geologic deposits through which water travels. The length of time water is in contact with hardness producing material helps determine how much hardness there is in raw water. Hardness was originally defined as the capacity of water to precipitate soap caused by Calcium and Magnesium.<br><br>
3. Solids(Totaldissolvedsolids-TDS):Waterhastheabilitytodissolveawiderangeof inorganic and some organic minerals or salts such as potassium, calcium, sodium, bicarbonates, chlorides, magnesium, sulfates etc. These minerals produced un-wanted taste and diluted color in appearance of water. This is the important parameter for the use of water. The water with high TDS value indicates that water is highly mineralized. Desirable limit for TDS is 500 mg/l and maximum limit is 1000 mg/l which prescribed for drinking purpose.<br><br>
4. Chloramines:Chlorineandchloraminearethemajordisinfectantsusedinpublicwater systems. Chloramines are most commonly formed when ammonia is added to chlorine to treat drinking water. Chlorine levels up to 4 milligrams per liter (mg/L or 4 parts per million (ppm)) are considered safe in drinking water.<br><br>
5. Sulfate:Sulfatesarenaturallyoccurringsubstancesthatarefoundinminerals,soil,and rocks. They are present in ambient air, groundwater, plants, and food. The principal commercial use of sulfate is in the chemical industry. Sulfate concentration in seawater is about 2,700 milligrams per liter (mg/L). It ranges from 3 to 30 mg/L in most freshwater supplies, although much higher concentrations (1000 mg/L) are found in some geographic locations.<br><br>
6. Conductivity:Pure water is not a good conductor of electric current rather’s a goodinsulator. Increase in ions concentration enhances the electrical conductivity of water. Generally, the amount of dissolved solids in water determines the electrical conductivity. Electrical conductivity (EC) actually measures the ionic process of a solution that enables it to transmit current. According to WHO standards, EC value should not exceeded 400 μS/cm.<br><br>
7. Organic_carbon:TotalOrganicCarbon(TOC)insourcewaterscomesfromdecaying natural organic matter (NOM) as well as synthetic sources. TOC is a measure of the total amount of carbon in organic compounds in pure water. According to US EPA < 2 mg/L as TOC in treated / drinking water, and < 4 mg/Lit in source water which is use for treatment.<br><br>
8. Trihalomethanes:THMsarechemicalswhichmaybefoundinwatertreatedwith chlorine. The concentration of THMs in drinking water varies according to the level of organic material in the water, the amount of chlorine required to treat the water, and the temperature of the water that is being treated. THM levels up to 80 ppm is considered safe in drinking water.<br><br>
9. Turbidity:Theturbidityofwaterdependsonthequantityofsolidmatterpresentinthe suspended state. It is a measure of light emitting properties of water and the test is used to indicate the quality of waste discharge with respect to colloidal matter. The mean turbidity value obtained for Wondo Genet Campus (0.98 NTU) is lower than the WHO recommended value of 5.00 NTU.<br><br>
10. Potability: Indicates if water is safe for human consumption where 1 means Potable and 0 means Not potable.<br><br>

## Framing the Problem and Looking at the Big Picture
### Frame the Problem
The dataset selected is a classification task, which means there is a category picked, in this case, if the water is potable or not. Through the use of supervised learning, meaning that the training examples are labelled, and batch learning, because of a small dataset, no continuous flow of data coming into the system and no need to adjust to changing data rapidly, the problem will be solved.<br>
The objective is to find a model that allows us to predict whether the water in a river is drinkable or not to know if we should invest in the development of a sanitation network of water.
This task will therefore be binary classification, we will assign in the remainder of this project the value 1 for “Drinkable” and 0 for “Non-Drinkable”

1. Supervisedlearning–trainingexamplesarelabelled.<br>
2. Aclassificationtask–predictacategory.<br>
3. Batchlearning<br>
  ● Small data set<br>
  ● No continuous flow of data coming into the system<br>
  ● No need to adjust to changing data rapidly<br>

### Missing values:
● ph: 491<br>
● Sulfate: 781<br>
● Trihalomethanes: 162<br>
### Duplicated values:
There are no duplicate values in the dataset.


### Look at the big picture
Predictions will be used to help inform people if the body of water is drinkable. This will be done through the following properties of the water: pH value, hardness, solids, chloramines, sulfate, conductivity, organic carbon, trihalomethanes, and turbidity.

## Description of the Dataset
The dataset for this project focuses on predicting the potability of water, where potability is represented as a categorical variable with values of 0 or 1. The primary goal is to develop a dependable prediction model based on nine numerical features. Each feature is of type float, indicating a numeric nature, and contributes distinct information to the analysis. Notably, the features exhibit variations in scale, reflecting their diverse measurement units.

