# Eluvio_DS_Challenge

 

## Problem Statement

The dataset is tabular and the features involved should be self-explanatory. We would like for you to come up with a specific problem yourself and solve it properly. This is an “open challenge,” mainly focusing on natural language processing. The problem could be either about predictive modeling or providing analytical insights for some business use cases. Note the problem should be treated as large-scale, as the dataset is large (e.g., >100GB) and will not fit into the RAM of your machine. Python is strongly recommended in terms of the coding language.

## Overview
Now assuming that the dataset is large that is >1000 GB. **Pandas** may not be a better choice considering RAM limitations we have in our systems. To overcome this problem we use **Dask** library here which works quiet similar to pandas.

To give an example how dask works, consider the case if we have 100GB data. Now if we do any row operation, then what Dask Dataframe do, it will breake the data into say 100 chunks. It will then bring in 1 chunk into the RAM, perform the computation, and send it back to the disk. It will repeat this with the other 99 chunks. If you have 4 cores in your machine, and your RAM can handle data equal to the size of 4 chunks, all of them will work in parallel and the operation will be completed in 1/4th of the time. The best part: you need not worry about the number of cores involved or the capacity of your RAM. Dask will figure out everything in the background and not give you any burden.

## Prerequisites & Importing libraries
- dask[complete]
- nltk
- seaborn

Install all the dependencies with pip command inside colab notebook.
```sh
!pip3 install (above prerequisite)
```
Import necessary libraries of Dask and NLTK with these commands
```sh
import nltk
from wordcloud import WordCloud


nltk.download('averaged_perceptron_tagger')
nltk.download('stopwords')
import dask.dataframe as dd
from dask.distributed import Client

client = Client(n_workers=4)
import pandas as pd
```

## Data Preprocessing
The following code load the data into dask dataframe,where using the <code>blocksize</code> will define how many memory should our RAM use.


```sh
from dask import dataframe as dd
df = dd.read_csv(
    '/home/aditya/euvio challenge/Eluvio_DS_Challenge.csv', 
    delimiter=',',
    blocksize=64000000 # = 64 Mb chunks
)
```
<code> <i>This text will be italic</i> <b>this text will be bold</b> </code>




## Inference
