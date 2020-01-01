FashionNet
-------------

## Description


FashionNet originated and diverged from [FashionNet](https://github.com/PlabanM1/FashionNet) is a fashion recommendation system capable of learning fashion styles and recommending accordingly through a simple deep learning algorithm.


*FashionNet is divided into 4 parts*


### Data training

**Each categories(Style, Pattern, Fabric, Color) has to be trained by changing the names of variables on the code.** 
Pictures on each categories are learned and saved as a weight file 'vgg_weights_best_*category*.hdf5'.

### Fashion tags

Using the weights processed from 'Data training' all sorts of pictures that has a singular fashion style and without any bizarre background can be easily categorized. The pictures that you want to categorize should be saved in the directory named 'scraped' (This directory can be altered simply by chaning the code).

### Vector maker

Fashion vectors made here are used further for 'Similarities'. Vector maker allows you to save a dataset of your own in numpy format that can be used when you will be looking for similar clothes. The numpy file holds the data of classes of each categories as numbers for each clothes (e.g. Clothes with attributes Checked, Chiffton, Green, Sports an array of (0, 0, 2, 3)). Only the clothes made and saved into the numpy format will be used for similarity checks so be sure to put the clothes of your comparisons in the path of 'retail' or change the code according to the path of your choice. For this I scraped some images from Korean online shopping malls for testing.

### Similarities

Similarities finds what clothes that are in a certain directory are similar to the clothes that are given(user's preferred style or maybe something out of their SNSs). Even tho multiple clothes can be used for *user's style* it is strongly recommended to use one or clothes with the same style tags. For every matching category a score goes up thus 4 is the maximum score that can be given while the score of 0 is the minimum. The top 5 similar clothes and their scores are shown.


### Versions

|Python|Tensorflow|Keras|CUDA|cuDNN|
|:---:|:---:|:---:|:---:|:---:|
|3.6|1.13.1|2.2.4|10.0|7.5|

### Dataset

*Dataset has around 40K classified images*

The Dataset has been made with images scraped from Google or retail stores.

You can download the full dataset and other files that I used from [here](https://drive.google.com/open?id=1Dxa82hVPExqtpfyZ6gHZrnS6080frMMk).

Thanks to [Minkyeong Kang](https://minkyeongkang.github.io/static_page), [Junhyeong Kim](https://junhyeongkim73.github.io/static_page), [Yerim Jeon](https://jyerim.github.io/static_page/) and [Hayoung Cho](https://wh28533.github.io/static_page/) on making the dataset.