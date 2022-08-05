# Emotion-Detection
This project is a basic classification project to test the results of 2 different classifier architectures over the fer2013 dataset which contains 48x48 black and white images and details about the emotion expressed in them (7emotions).

Frameworks Used: PyTorch, NumPy, Pandas, Matplotlib.

Preprocessing:

![image](https://user-images.githubusercontent.com/74304695/183113285-7229649a-1d8a-4841-a2fc-c0f8db6e24e4.png) 
![image](https://user-images.githubusercontent.com/74304695/183113318-1ddc8df8-1bd1-424d-ad60-914b21dac230.png)

Preprocessing of images involves a simple normalization of images and separation into Training, PrivateTest and PublicTest datasets 

![image](https://user-images.githubusercontent.com/74304695/183115432-ef10e49b-a0dc-4c4c-af7b-0fa6ae698efd.png)
![image](https://user-images.githubusercontent.com/74304695/183114439-a327d41c-82ec-49be-bb64-b646d11b4ba0.png)

Using a 7 convolutin and 3 resolution net with a cyclic, triangular learning rate, which a frequency of 10 epochs results in a validation accuracy of 62% and a test accuravy of 61%, however the accuracy and learning rate stagnate around epoch 25. 


![image](https://user-images.githubusercontent.com/74304695/183115497-b9b736f3-43df-4883-90f8-be4182fabad1.png) 
![image](https://user-images.githubusercontent.com/74304695/183115159-05cd1fd4-164f-4461-81df-015eaf39b763.png)

Decreasing the number of convolutions to 5 and the number of epochs to 25 results in a significantly better accuracy of 65% in validation and 63% in testing.

LIMITATIONS:
1. The primary limitation of the model is the usage of monochrmatic data, this is resulting in overfitting of the training data with a training accuracy hittting 99.8%.

The state-of-the-art accuracy in this project is 70%, hence an accuracy of 65% is deemed good.

IMPROVEMETS: 
1. Using coloured images
2. testing different variations in learning rates. 
