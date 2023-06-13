<h1>RapidMiner - Bank Default Prediction</h1>


<h2>Description</h2>
Project consists of importing a CSV file and fixing the class imbalance from the dataset. The data is cleaned up by selecting attributes, setting role, sampling the data and then splitting it to run the test and training data. Trying to find the best predictors to see if someone will default on a loan.
<br />


<h2>Predictive Methods Used</h2>

- <b>Batch Prediction</b>
- <b>Ensemble through Voting</b> 
- <b>Bagging with Rule Induction inside</b>
- <b>Random Forest</b>

<h2>Materials Used </h2>

- <b>RapidMiner</b>
- <b>CSV file</b>

<h2>Project walk-through:</h2>

<p align="center">
Knowing your data: <br/>
<img src="https://imgur.com/jiPkQ4W.png" height="80%" width="80%" alt="Project walk-through"/>
<br />
<br />
Default confusion matrix:  <br/>
<img src="https://imgur.com/ZQKVbE3.png" height="80%" width="80%" alt="Project walk-through"/>
<br />
<p align="left">
<br />
 There is a big class imbalance issue for Default. There are 9378 total values for default and 9165 are for “no”. That means that 97.73% of the values for default are heavily leaning towards no. This is bad because some machine learning algorithms could be biased and inaccurate. It is hard for them to take into class distribution/their proportions. Also, housing has a lot more yes values than no.

 In the data set the default label when ran has 2749 no values and 64 yes values and a proportion of 97.7% no values. Default has a 99.71% true no percentage, and a true yes prediction has a 4.69% prediction. The pred of no was 97.82% while the prediction of yes was 27.27%. There is a big imbalance as the prediction for yes was only predicted 11 times and was right just 3 times.

The class imbalance is important because the bank only predicted yes 27.27% correct and they only predicted yes 11 times out of the 2813 predictions. This means the bank over looked the 61/64 yes values. That is not good when predicting who defaults.
<br />
<p align="center">
<br />
Resampling to fix class imbalance: <br/>
<img src="https://imgur.com/MWGpZDl.png" height="80%" width="80%" alt="Project walk-through"/>
<br />
<br />
New confusion matrix:  <br/>
<img src="https://imgur.com/g0NbPg4.png" height="80%" width="80%" alt="Project walk-through"/>
<br />
<p align="left">
<br />
The overall accuracy with a balanced number of different values in the new model went down to 68.33%. The class precision went way down, but it is a lot more balanced having both within a few percent of each other.  Rather than yes only being predicted yes 11 times it was now predicted a total of 56 times. The class recall is down for true no while it is up considerably for true yes. This is good as the data is more balanced and the correct predictions for those who default are up. The precision is good for seeing how accurate each prediction of no and yes were while recall is good for seeing how the true predictions were in the model.
<br />
<p align="center">
<br />
Setting up the first prediction:  <br/>
<img src="https://imgur.com/bqT7WbM.png" height="80%" width="80%" alt="Project walk-through"/>
<br />
<br />
Batch Prediction:  <br/>
<img src="https://imgur.com/xKQ7djd.png" height="80%" width="80%" alt="Project walk-through"/>
<br />
<br />
Ensemble Voting:  <br/>
<img src="https://imgur.com/niakFK4.png" height="80%" width="80%" alt="Project walk-through"/>
<br />
<br />
Bagging with Rule Induction inside:  <br/>
<img src="https://imgur.com/vHZu98Q.png" height="80%" width="80%" alt="Project walk-through"/>
<br />
<br />
Random forest:  <br/>
<img src="https://imgur.com/cwRRea6.png" height="80%" width="80%" alt="Project walk-through"/>
<p align="left">
<br />
After fixing the class imbalance four different methods were used to help the model's accuracy. All the new matrices after fixing the class imbalance were better in all the class recalls and class precisions. The best decision was the random forest. The random forest was better at predicting yes and no. It was higher by at least 10% for those predictions. The class recall for true no and true yes were also better by a large margin of at least 10% for both again. The overall accuracy of the random forest was 80.83% compared to the matrix that was fixed after the class imbalance 68.33%. That is a substantial margin.
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
