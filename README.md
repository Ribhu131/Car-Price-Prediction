# Car-Price-Prediction
Car Price Prediction Challenge
Overview:


Cars are more than just a utility for many. We all have different tastes when it comes to owning a car or at least when thinking of owning one. Some fit in our budget and some lauxury brands are heavy on our pockets. But that should not stop us from owning it, atleast used ones. The goal of this project to predict the costs of used cars to enable the buyers to make informed purchase using the data collected from various sources and distributed across various locations in India.

Dataset Descrption:


Collected From Kaggle Dataset.

Attribute Information:


Name: The brand and model of the car.
Location: The location in which the car is being sold or is available for purchase.
Year: The year or edition of the model.
Kilometers_Driven: The total kilometres driven in the car by the previous owner(s) in KM.
Fuel_Type: The type of fuel used by the car. Transmission: The type of transmission used by the car.
Owner_Type: Whether the ownership is Firsthand, Second hand or other.
Mileage: The standard mileage offered by the car company in kmpl or km/kg
Engine: The displacement volume of the engine in cc.
Power: The maximum power of the engine in bhp.
Seats: The number of seats in the car.
New_Price: The price of a new car of the same model.
Price: The price of the used car in INR Lakhs.

key technical aspects:


After data exploration and visualization various data prepossing steps are selected after of data. Following are noticeable ones among them.

New_Price feature dropped due to significant missing values.
Name column split into Brand and Model features.
Continuos variables including target feature are Log transformed to make their distribution symetrical.
Kilometers_Driven and Mileage are multiplied together to form new feature as this interaction show high correlation with target feature price.
Brand,Model, and Location are encoded using Target encoding as they have lot of categories.
Fuel_Type, Transmission, and Owner_Type are one-hot encoded.
Year columns are deducted by current year to introduce aging effect (current year - edition year).

Best Model selection:


The data is trained on Linear Regression, KNN, SVM, Decision Tree,Random Forest, GBDT and XGBoost with hyper-parmeter tuning. GBDT turns out be best model with lowest loss of 0.033.

Metric:
Root Mean Squared Logarithmic Error (RMSLE) is used as metric.
RMSLE is usually used when you don't want to penalize huge differences in the predicted and the actual values when both predicted and
true values are huge numbers. Rather we have to focus on percent error relative to the actual values.


