# XGBClassificationQuartic


Cleaned Dataset: 

Time Stamp seperated to Features--> m (month) , date, year, hr, min , mari(AM/PM)
(ELIMINATED "SECONDS" FEATURE)
11 Features used:
m	date	year	hr	min	mari	FeaA	FeaB	FeaC	FeaD	FeaE


Results On Trainset :
Confusion matrix,

           class   0       1     2       3      4

Predictions
	           0	[[105609     16   6080   1760   1961]
 	           1	[   390 219213     37   1422      0]
 	           2	[   995      6 303083     14    115]
 	           3	[   387    324    130 124208     45]
 	           4	[  2406      2    690    567  30540]]
Individual 
Class Accuracy-->96.19%  99.84%  97.76% 97.06% 93.51%		    				


Overall Trainset accuracy -> 97.83%  (Diagonal elements/total)


Furthermore :

1.If Test set accuracy drops alot, model might be overfitting:
Solutions--> 
            
	    a) Add Data
	    b)Introduce regularization Parameter OR 
	    c)Reduce features
	    d)Test set might be coming from different distribution so add that distribution's examples to train set
	    
2.Examine individual class performace:
  Example, Class 4 prediction performing worst as per train accuracy(93.51%):
  Solutions-->  
  
	  a) Add more class 4 dataset examples
          b) Check whether True labels are correctly labelled

3. Is human level accuracy not yet reached?
   Solutions--> 
   
   	   a) Cross validation set, to tune Hyper-Parameters
 	   b) Introduce new features
	   c) Add Data	
