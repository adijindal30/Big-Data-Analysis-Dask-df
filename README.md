# Eluvio_DS_Challenge

 

## Problem Statement

The dataset is tabular and the features involved should be self-explanatory. We would like for you to come up with a specific problem yourself and solve it properly. This is an “open challenge,” mainly focusing on natural language processing. The problem could be either about predictive modeling or providing analytical insights for some business use cases. Note the problem should be treated as large-scale, as the dataset is large (e.g., >100GB) and will not fit into the RAM of your machine. Python is strongly recommended in terms of the coding language.


## Prerequisites & Importing libraries
- dask[complete]
- nltk
- seaborn

Install all the dependencies with pip command inside colab notebook.
```sh
!pip3 install (above prerequisite)
```

## Data Preprocessing
Based on **Data Preprocessing.ipynb** notebook.
For prepairing the training and testing data we extract the MFCC features from the audio files

```sh
y, sr = librosa.load(file_loc,sr = 22050,offset = start+i*audiolen, duration = audiolen)
mfcc = librosa.feature.mfcc(y=y, sr=sr)
```




## Inference
For training we use tensorflow sequential models.
]
[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>
