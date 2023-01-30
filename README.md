# KurdishMusicGenreRecognition
A dataset of for Kurdish Music Genre Recognition

The dataset was collectedy by: Aza Kamal

The Kurdish Music Gnere Recognition and the datset are explained in the following article:

[Kurdish Music Genre Recognition Using CNN and DNN](https://sciforum.net/paper/view/13803)

[Comparing the Accuracy of Deep Neural Networks (DNN) and Convolutional Neural Network (CNN) in Music Genre Recognition (MGR): Experiments on Kurdish Music](https://arxiv.org/abs/2111.11063)

Please cite when you use the dataset cite the realated article as follows:

Kamala, A.; Hassani, H. Kurdish Music Genre Recognition Using CNN and DNN, in Proceedings of the 3rd International Electronic Conference on Applied Sciences, 1–15 December 2022, MDPI: Basel, Switzerland, doi:10.3390/ASEC2022-13803

Zuhair, A. and Hassani, H., 2021. Comparing the accuracy of deep neural networks (DNN) and convolutional neural network (CNN) in music genre recognition (MGR): experiments on Kurdish music. arXiv preprint arXiv:2111.11063.

Notice: The whole dataset is very large, therefore we have selected a subset of the data.
This compressed file has two JSON files inside:
1. extracted_feature_dataset_1_s.json (this is the selected subset of the dataset that was for 1-second long audio. It has a total of 2000 data, 250 data per genre.) (22 MB)
2. extracted_feature_dataset_25_ms.json (this is the selected subset of the dataset that was for 25 milliseconds long audio. It has a total of 40000 data, 5000 data per genre.) (20 MB)

The keys inside each JSON file:
mapping: This key holds a list of the genre names with respect to the data order in the "labels" and "mfcc" keys. For example, "halparke_dagha" is the first genre in this list, then the value (0) in the "labels" key refers to "halparke_dagha".

mfcc: This key holds a list of the extracted features of each audio that was used for the trained models.

labels: This key holds a list of all the "mfcc" key labels, which means the indexes in this list correspond with the indexes in the "mfcc" key list. For example, index 1 in the "mfcc" key list is the extracted feature for the "halparke_dagha" genre (which is label 0), then index 1 in the "labels" key list is 0 (which is "halparke_dagha").

Since we have two different types of datasets, one for 1-second long audios and one for 25 milliseconds. I had to create two different subsets for each one. Just want to indicate that these two JSON files are not randomized, they are in order of the "mapping" key (the genres) inside the JSON file. This means the data starts with label 0 and until label 7.
