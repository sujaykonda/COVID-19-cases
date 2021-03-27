# This is a COVID-19 Model  
## Important Notice, these weren't super accurate but they are just for learning purposes  
This data model finds the peak of the number of COVID-19 cases, the number of people interacting, and the interaction rate among people. This data model is built in Python.  

## Overview of the Data Model  
1. First the model gets the data from csv files. You can download the csv files from kaggle.com
2. The model then processes the data
3. The model then tunes params in a simulation function using nelder mead a very simple optimization method which literally triangulates the parameters
    1. The params are InitialP, interaction_rate, population (population is the number of people who are interacting)
    2. The simulation function uses this equation to find the change in number of cases:  
    ![Math](http://www.sciweavers.org/tex2img.php?eq=%20%5CDelta%20p%20%3D%20%20%5Clambda%20%281-p%29&bc=Black&fc=White&im=jpg&fs=12&ff=arev&edit=0)
    3. It also used scipy.optimize.minimize, with method = nelder mead

## Rest of the Code
https://github.com/sujaykonda/COVID-19-cases/blob/master/COVID-19.ipynb

## Extra Notes
If you want to run this on your own computer, just download the zip and you can play around with it!
It does take a decent amount of time to tune but no gpu was used.
