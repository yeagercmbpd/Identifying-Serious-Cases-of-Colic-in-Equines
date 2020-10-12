<p align="center">
   <img src=https://github.com/yeagercmbpd/Identifying-Serious-Cases-of-Colic-in-Equines/blob/main/Images/Project%201%20Banner.png>
<div align="center">
   <figcaption></figcaption>
</div>
</p>

Identifying Serious Cases of Colic in Equines
---
Logistic Regression classifier for identifying cases of colic in horses which may result in required surgery or death, based on animal evaluation by a veterinarian.

---
### Overview and Project Goals
Colic is a broad term used to describe gastrointestinal distress in horses. It often has a sudden onset and can be caused by a myriad of reasons. It is not always easily identified and the seriousness of the problem can often escalate quickly and lead to necessary surgical intervention and often times death of the animal. The American Horse Council advises that colic causes the death of approximately 64,000 horses in the United States annually. An otherwise healthy horse can begin to show signs and symptoms which can, in a matter of hours, escalate severely. Yeager Biomedical Solutions has created a Logistic Regression Classifier model to assist equine facility staff, as well as veterinarians in identifying cases in which horses are at high risk of death, as well as cases in which surgical intervention may be an optimal solution. The model takes into account medical evaluation data from the subject and produces an output whereby death or surgery are the likely outcomes. 

---
### Repository Navigation
<pre>
Data Cleanup  : <a href=https://github.com/yeagercmbpd/Identifying-Serious-Cases-of-Colic-in-Equines/blob/main/Notebooks/Project%201%20Data%20Preparation.ipynb>Data Preprocessing Notebook </a>
Model Building: 
<a href=https://github.com/yeagercmbpd/Identifying-Serious-Cases-of-Colic-in-Equines/blob/main/Notebooks/Logistic%20Classifier%20for%20Death%20Outcome.ipynb>Building the Death Outcome Model Notebook</a>
<a href=https://github.com/yeagercmbpd/Identifying-Serious-Cases-of-Colic-in-Equines/blob/main/Notebooks/Logistic%20Classifier%20for%20SurgicalOutcome.ipynb>Building the Surgery Outcome Model Notebook</a>
Visualizations: <a href=https://github.com/yeagercmbpd/Identifying-Serious-Cases-of-Colic-in-Equines/blob/main/Notebooks/ExploratoryVisualizations.ipynb>Visualizations Notebook</a>
Technical Notebook: <a href=https://github.com/yeagercmbpd/Identifying-Serious-Cases-of-Colic-in-Equines/blob/main/Technical%20Notebook-Final.ipynb>Technical Notebook</a>
</pre>
---
### ReadME Navigation

[Data](https://github.com/yeagercmbpd/Identifying-Serious-Cases-of-Colic-in-Equines/tree/main/Data) -
[Results](https://github.com/yeagercmbpd/Identifying-Serious-Cases-of-Colic-in-Equines#Summary) - 
[Project Info](https://github.com/yeagercmbpd/Identifying-Serious-Cases-of-Colic-in-Equines#PackagesandCredits) -

---

## The Data
This dataset used in this analysis is located on the UCI machine learning repository [https://archive.ics.uci.edu/ml/datasets/Horse+Colic](https://archive.ics.uci.edu/ml/datasets/Horse+Colic). The data for a study like this is fairly rare and additional sources proved difficult to locate. This data consists of 368 records of horses which were evaluated by veterinarians. This information was then compiled by the University of Guelph. While small, a total of 27 features are included with each record to assist in bolstering the strength of the dataset for model creation.

---

## Features and Limitations 
Features are reported in various formats, including continuous  and categorical and include the following: 

surgery outcome, Age, Hospital Number, rectal temperature, pulse, respiratory rate, temperature of extremities, peripheral pulse, mucous membranes, capillary refill time, pain  as a subjective judgement of the horses pain level, peristalsis, abdominal distension, nasogastric tube, nasogastric reflux, nasogastric reflux PH, rectal examination  feces, abdomen, packed cell volume, total protein, abdominocentesis appearance, abdomcentesis total protein, outcome, surgical lesion, and type of lesion.

Our target variables in the creation of this model will be outcome, whether the horse lived or died, and surgical lesion, whether the colic case was found to have been a candidate for surgery.
   
The main limitation of this dataset, alluded to above, is the relatively small sample size. Unfortunately additional datasets to incorporate into this one could not be located. Additionally, due to the difference in operating procedure by the veterinarians, some fields are left blank or not used in some cases. Fields with extremely high null values counts (greater than 25%) were excluded in some cases. Other features, where possible were extrapolated or filled using mean/median values to account for null values.

---

## Summary

Model 1 Predicting Death Outcome
   Test Accuracy: .79
   10-fold Cross Validation: .74
   Features Used:Pulse,Respiratory rate,Pain level,Packed cell vol,Type of lesion
   Holdout Accuracy: .84
   
Model 2 Predicting Required Surgery
   Test Accuracy: 1
   10-fold Cross Validation: 1
   Features Used: surgery,pulse,temperature of extremities,peripheral pulse,mucous membranes,capillary refill time,pain level,peristalsis,abdominal distension,packed cell volume,type of lesion,location of lesion
   Holdout Accuracy: .52

The goal in creating our models was to give veterinarians and equine care staff an additional tool in gauging the severity of suspected colic in horses under their care. A reasonable level of accuracy has been achieved, given our limited data set, in attaining that goal. A rapid evaluation of the sick animal can be entered into our models to determine the severity of the illness and validate the decision to aggressively treat, and hopefully save the patient. The tough decision to commit to surgery and reduce the percentage of horses which perish from a lack of this intervention is our hope. With adoption of this model and an increase in observations, its strength in making accurate predictions can only increase.

---

## PackagesandCredits
<pre>
By : <a href=https://github.com/yeagercmbpd>Christopher Yeager</a>
</pre>

<pre>
Languages    : Python
Tools/IDE    : Jupyter
Libraries    : pandas, numpy, matplotlib, sklearn, seaborn
</pre>
