Metal Casting product image classification for quality inspection using Pytorch.


What is Casting?
Casting is a manufacturing process in which a liquid material is usually poured into a mold, which contains a hollow cavity of the desired shape, and then allowed to solidify.

Types of casting defects:
There are many types of defect in casting like blow hole, pin hole, burr,shrinkage defects, mold material defects, pouring metal defects, metallurgical defects, etc.

Objective of this project:
The objective of this project is to automate the process of finding defects in the casting process. A casting defect is an undesired irregularity in a metal casting process. For removing this defective product all industries have their quality inspection department. But the main problem is that this inspection process is carried out manually. It is a very time consuming process and due to human error the proces of rejecting defects is not 100% accurate.This can be the cause of rejection of an entire order which would lead to huge losses. Our model will try to eliminate this loss of revenue and make the QC process as accurate as possible.

Dataset used for this project:
Casting products image dataset

Type of data:
The problem is an image classification problem. We have a train dataset having 6633 images and test dataset of 715 images

Type of problem:
Image classification with two outputs

Modeling
Type of model	Batch Size	Number of epochs	learning Rate	Accuracy (On testset)	Time Taken	Notebook
Logistic Regression	16	10	0.0001	64.99%	10:01	Logistic Regression Model
Feedforward Neural Network	16	10	0.0001	75.6%	3:56	Neural Network model
Convolutional Neural Network	16	10	0.0001	99.86%	14:01	CNN Model
Observations
Logitic Regression
Loss graph	Accuracy Graph
	
The training usinng the logistic regression was very eratic compared to other models.
We got the least accuracy of 64% on the test set using logistic regression which was expected.
Logistic regression performs better when the data IS text based and not image based.
Compared to the CIFAR-10 image set, logisitc regression did better with this image set. This probably is because of lesser number of classes and higher resolution images.
Feed Forward Neural Network
Loss graph	Accuracy Graph
	
Much smoother in terms of reduction of loss and increase in accuracy.
Since this is a simple classification problem I used a simple neural network with 2 hidden layers and an output layer.
It was expected that this model will perform better than logistic regression.
Neural Networks take chunks of the image data and make them into nodes.
This probably gives the machine a better chance at being able to differentiate between a defective product and an ok product.
We got an accuracy of 79% on the test set which was an improvement over the logistic regression model.
Convolutional Neural Network
Loss graph	Accuracy Graph
	
CNN had to do better than the traditional neural network because it is known for image classification problems.
It slides a ‘nxn’ matrix specified by us over the entire image and assigns weights. Read here to know more about CNN.
We were able to achieve an amazing accuracy of 99.86% on the test set.
This high accuracy was probably because we had only two classes and secondly the inspection is of only one part. Hence there is more unifornmity between the images and it is easier to detect faults.
Conclusions
This project helped me understand how useful deep learning and image classification can be in real industries. Inspection and quality control is an aspect I have observed in all my past internships. Whether it be with robotic systems or welding processes. An advantage of ML and DL models is that it can be implemented on other image sets with minimal changes. This makes it much more advantageous and is now the new way of programming.

For future work, this project could be a game changer for quality control in heavy machinary industries. However adopting this in the industry could take sometime due to infrastructure requirements like cameras and a set process which would automate the Quality Control process.
