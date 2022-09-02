# Create a credit risk analysis report 
## Random_Over_Sample_Analysis

credit risk analysis report is a classification problem: because there is outnumbered healthy loans than risky loans we need to make split 
with Logistic regression model to compare oroginal data with resample data

# Step1:
## Imports
Libraries has been used to read csv file uploaded from starter_code folder, displays plots and Trainmodel, predit and Evaluate
![Screenshot 2022-09-021](https://user-images.githubusercontent.com/69637182/188212561-8c0dc474-0ae4-4850-8943-1ca0e24cf093.png)
![Screenshot 2022-09-02 1308382](https://user-images.githubusercontent.com/69637182/188212936-4b9a5649-085c-424d-be86-e9e1d75c99b5.png)

Apply info, describe methods to get general idea about dtypes, and if our data evenly distributed we can check with describe method
showing below:
![Screenshot 2022-09-02 1313403](https://user-images.githubusercontent.com/69637182/188213785-35d577a0-b057-4d7b-928b-fef2c8f5c51a.png)
![Screenshot 2022-09-02 1314034](https://user-images.githubusercontent.com/69637182/188213799-3ebb68fa-3a75-487f-b1fa-50b8c7ac6e1c.png)
 ## Visualize Date if it has a normal distribution by using seaborn pairplot then look into diagonal matrix:
 ![Screenshot 2022-09-02 1316245](https://user-images.githubusercontent.com/69637182/188214062-6adc154a-4aaa-485d-a92a-5ec21b98b477.png)
 
# Step2:
Apply supervised learning (logistic regression model)  on our original data, before that we need to scale X_train, X_test to make them between 0 and 1 by using 
import model StandardScaler then fit X_train then transform X(train,test), the output is two dimentional arrays X_test_scaled, y_train_scaled
![Screenshot 2022-09-02 1330026](https://user-images.githubusercontent.com/69637182/188216020-262947eb-b301-42d8-b161-683fc250804f.png)

After we done by train_test_split our model we to Predict, store it into a new data frame the plot it, Evaluate out prediction by calulating 
![Screenshot 2022-09-02 1336557](https://user-images.githubusercontent.com/69637182/188217051-b720b3b7-760b-4bfd-a845-49a0b1560b2c.png)
![Screenshot 2022-09-02 1338388](https://user-images.githubusercontent.com/69637182/188217286-0efc279b-8078-4f70-b570-f0687f7e90f4.png)

accuracy_score 
confusion matrix 
classification report

# Step3:
In this step we use RandomOverSample method as suggested, by applying Counter on y_train wich is our target we can see there is imbalanced numbers between
loan healthy and loan defaulting, then when we apply ROS method we will bring lowest number to highest then we make our prediction, basically is the same steps
as instructed in step2, so we are trying to show which model perform better results, but in reality both of them are leading to perfect precision and accuracy
![Screenshot 2022-09-02 1347169](https://user-images.githubusercontent.com/69637182/188218637-b6f7ebd8-0756-458c-9942-88e189073694.png)

# Conclusion
Both models outputted same results so I would recommend them both for classification problems analysis. 
