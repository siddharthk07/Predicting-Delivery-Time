

We have been asked to predict the time taken from variable Origin, destination and Type.
None of these variable have been explicitly specified in the dataset and have been jumbled up in one single “details column” Hence this requires a lot of cleaning. 

The only worthwhile feature I believe can be extracted from Origin and Destination is the distance between them. More distance should theoretically take more time. For this I used the Google API to get the latitude and longitude Of the Places and used the heaviside formula to calculate the Distance between them

For the variable to be predicted,  I extracted the origin and delivery dates and used it to calculate the time taken.

Feature Engineering - 
 

1)We can pullout the number of sub-stops between origin and destination using the “details” column. Substops is directly proportional with time taken to deliver as number of substops will increase time.
2)We can find out distance between the two locations using Google API and use that as a feature.I cant think of a way other than this to use it as a feature
3)Time taken can be pulled out from the “details” column. This is the output variable to predict.
 


I personally feel that number of substops is the best predictor of the number of days, because even though distance can somewhat predict time, it does not take it account things like package being stuck at the courier centre and the customer delaying delivery and what not. All this is accounted by number of substops. Together they can be powerful predictors however the questions states only to use origin, destination, type of package.


