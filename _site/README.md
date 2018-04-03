# 3D-Gait-Recognition

Creating a deep learning pipeline for the identification of the person by the manner of its walking i.e. using his/her gait features.

![Gait Recognition](/assets/img/post/gait.png)

## Dataset
The dataset that we will be using in the project will be the Human3.6M dataset. The dataset consists of 3.6 million different human poses collected with 4 digital cameras.

## Proposed Edge Device
Nvidia Jetson TX2
![Nvidia Jetson TX2](/assets/img/post/jetson.jpg)

## Proposed Pipeline
1. Identifying and creating the Ground Truth data.
2. Getting the individual poses for each of different concerned objects in each frame.(DensePoseRCNN)
3. Establishing the spatio-temporal relationships between the frames in the gait cycle using
RNNs or LSTMs.
4. Optimizing the above network by creating TensorRT engine to work on the Nvidia Jetson .Tx2

## About
The Assignment's aim is to develop human recognition system via gait features. This Assignment was under Prof. [ Aditya Nigam](http://faculty.iitmandi.ac.in/~aditya/).

## Contributors

[Abhijeet sharma](http://students.iitmandi.ac.in/~abhijeet_sharma)
1. Github: http://github.com/abhijeet2096
2. Email: sharma.abhijeet2096@gmail.com
3. Mobile: +91-8629015433

[Mohit sharma](https://www.facebook.com/profile.php?id=100009376469653)
1. Github: https://github.com/mohitsharma1996
2. Email: mohit21sharma.ms@gmail.com
3. Mobile: +91-8629015362

[Akhil singhal](https://www.facebook.com/akhilsinghal1234)
1. Github: https://github.com/akhilsinghal1234
2. Email: akhilsinghal1234@gmail.com
3. Mobile: +91-8629015410
