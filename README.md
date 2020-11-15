# ADM-Homework-2

_Group 23 is  formed by:_

* Alessandro Quattrociocchi (1609286)
* Edoardo Ulrich Proverbio (1658119)
* Michele Amoroso (1760027)
 
 
 Our work aims to evaluate the operations that users perform on an ecommerce, in particular, we want to highlight the average number and type of operations that each user performs. 
 
 ## How we handled the data
 
 The size of each month was substantial (many GB), so a first analysis was done considering only a limited number of lines. Then the whole database was fully loaded and the code was tested in a more critical and stable way.  
The simulation of the complete database, however, took a long time, so we decided to use the complete dataset
only for operations that required it ("views", "cart" and "purchase").  
For most of the requests  we used the following approach:  
we have created a new database with the same structure as the first one, considering only the type of event "purchase". 
In fact, as shown by the pie chart at the beginning of the assignment, this event is only present in a small percentage compared to the number of views and carts.   
This approach made operations much faster than before and allows us to extend to extend the analysis to the complete data set. 


With the following terminal commands we have created a file with only sales data.
The first line is used to create an empty database, named ***Sales*** with the same structure as the columns of the whole dataset. 

***head -n 1 2019-Oct.csv  > Sales***

The following lines add the event type purchase for each month.   

***cat 2019-Oct.csv | grep purchase >> Sales***

***cat 2019-Nov.csv | grep purchase >> Sales***

***cat 2019-Dec.csv | grep purchase >> Sales***

***cat 2020-Jan.csv | grep purchase >> Sales***

***cat 2020-Feb.csv | grep purchase >> Sales***

***cat 2020-Mar.csv | grep purchase >> Sales***

***cat 2020-Apr.csv | grep purchase >> Sales***


## Get data to analyse 
### Download dataset

We downloaded from this links:   

* [This link](https://www.kaggle.com/mkechinov/ecommerce-behavior-data-from-multi-category-store?select=2019-Oct.csv)
for the months of October, November.    

* [This link](https://drive.google.com/drive/folders/1Nan8X33H8xrXS5XhCKZmSpClFTCJsSpE)
for the months of December, January, February, March and April.

We generated one versions of Sales Dataset: 

* [This link](https://drive.google.com/drive/u/0/folders/1R2GtHlhmNn-DDjLBxV9bNMK-kkwlubtN) for the extended version
for the months of October, November,December, January, February, March and April.



