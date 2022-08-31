Module 14 Challenge

In this project, a baseline for an algorithmic trading strategy is established.  Parameters are then ajdusted, including the SMA short, the SMA long,
and the size of the training data.  Different classifiers are also explored, with a new machine learning model being trained and the results compared
to the original models results.

---



## Technologies


This project uses Python 3.9.7 and the following libraries - 


| Library | Version | Documentation
|----|----|---|
| pandas |1.4.2| [pandas docs](https://pandas.pydata.org/docs)
| numpy |1.23| [numpy docs](https://numpy.org/doc/)
| sklearn | 1.1.2 | [sklearn docs](https://scikit-learn.org/stable/)


---



## Installation Guide



```
pip install -U scikit-learn

pip install numpy

from pandas.tseries.offsets import DateOffset
from sklearn import svm
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import classification_report
from sklearn.ensemble import AdaBoostClassifier
from sklearn import model_selection
```


---

<br/>

## Model Results

<br/>

# Baseline

**The baseline model had good results, showing an ability to beat the actual results from 2019 to 2021. It did show a poor recall and f-1 score for the -1 results.**

<p align="left"><img src="images/svm_base.JPG"></p>

<br/>
<br/>

# 6 Month Model

**The 6 month model followed the actual results well early on. It underperformed from 2019 to 2021 but was able to beat the actual returns after. This model also had a poor recall and f-1 score for the -1 results.**

<p align="left"><img src="images/svm_6_month.JPG">

<br/>
<br/>

# SMA Short-8 SMA Long 150

**With the SMA short and long increased the Strategy Return was able to match closely with the actual returns but showed little ability to beat the actual returns**

<p align="left"><img src="images/svm_8_150.JPG">

<br/>
<br/>

# Ada Baseline

**The Ada baseline model moved similar to the 6 month model. It showed a small increase in the reacall and f-1 score fro the -1 results but failed to perform well from 2019 to 2020. It had good results for 2021.**

<p align="left"><img src="images/ada_base.JPG">

<br/>
<br/>

# Ada Tuned Model

**The Ada tuned model showed the best results.  It greatly improved the reacall and f-1 for the -1 results but this came at a cost as the recall for the 1.0 results dropped.  It performed well through 2019 and had great results for the fisrt half of 2020.  Further adjustments could be made to the SMA's and data size to help correct the drop through the second half of 2020.

<p align="left"><img src="images/ada_tune.JPG">

---

<br/>

## Contributors

Dan McQueen

dandmcqueen@gmail.com

[Linkedin](https://www.linkedin.com/in/dan-mcqueen-4a5980238/)

---



## License

[GNU v3.0](LICENSE)
