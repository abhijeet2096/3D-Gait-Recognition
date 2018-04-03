---
# Posts need to have the `post` layout
layout: post

# The title of your post
title: Introduction

# (Optional) Write a short (~150 characters) description of each blog post.
# This description is used to preview the page on search engines, social media, etc.
description: >
  INTERIM PROGRESS REPORT

# (Optional) Link to an image that represents your blog post.
# The aspect ratio should be ~16:9.
image: /3D-Gait-Recognition/assets/img/default.jpg

# You can hide the description and/or image from the output
# (only visible to search engines) by setting:
# hide_description: true
# hide_image: true

# To enable comments on site
comments: true
# author tag
author: author4
# (Optional) Each post can have zero or more categories, and zero or more tags.
# The difference is that categories will be part of the URL, while tags will not.
# E.g. the URL of this post is <site.baseurl>/hydejack/2017/11/23/example-content/
categories: [Introduction]
tags: [firstpost, introduction]
# If you want a category or tag to have its own page,
# check out `_featured_categories` and `_featured_tags` respectively.
---

Biometrics has quickly entrenched itself as the most pertinent means for identifying and au-thenticating individuals.  The traditional methods no longer ensure the security of our data inthe hands of unauthorised persons.  Biometric use unique traits of an individual for its identi-fication. The biometrics can be broadly classified into two types namely wiz, 1) Physiological and 2) Behavioral biometrics.  The former includes the passive features like the fingerprint,iris,  face,  hand veins patterns etc and the later includes are active like gait,  signature voiceetc.  The physiological traits of an individual are highly unique and discriminant and thus arehighly  reliable.   The  physiological biometrics  require the  cooperation of  the individual  andalso a fully controlled setup for its high reliability.  Compared to the conventional biometrics,the behavioural traits are non-invasive, non-contact and are perceivable from a larger distance.This kinds of traits do not require a cooperation of the individual,  unlike the physiologicaltraits. Because of these advantages, these features gait recognition can be applied in scenarioslike surveillance, criminal investigation and access control.  Gait recognition can be affectedby many factors including pose variability, clothes, bags etc. All these factors make it a reallychallenging problem to solve.

The majority of the research work done primarily focuses on developing the novel algo-rithms for the recognition tasks or improving efficiency and accuracy of existing solutions.These  solutions  are targeted  over general  purpose processors  that are  expensive,  large  withhigh computational power and space.  Since gait recognition has a large search space and hasan extensive amount of computationally intensive operations, it is reasonable to suggest an em-bedded implementation specifically optimized to detect humans. An embedded solution wouldhave many many advantages including like low cost and integration within the embedded de-vices.  Embedded devices have hardware limitations, less GPU and memory so these modelsare hosted on the cloud. Embedded devices utilise these models by sending the input data ontothe cloud. These cloud-based implementations restrict the use cases i.e device must have inter-net connectivity, data privacy etc.  In order to overcome these restrictions, we need to deploythese onboard. For that model, optimization is needed to make it work on the Embedded deviceM

# Background

Gait is the study of the human locomotion or in other words, it's the manner in which you walk and run. Gait features are an important bio-metric feature for the human identification. It has demonstrated an immense potential for use in the human identification systems. It has been seen that every individual has a particular style of walking which can be used as an important trait to distinguish him from other humans. This has been used for the identification since a long time.  The suitability of the gait for the human identification is because it can be perceived from a distance as well as to its non-invasive nature. A huge amount of work has been done in the field of gait recognition. There are two major approaches to the problem one being the model-free approach and the other is the model-based approach.

**Model-Free Approach** In this approach, the silhouette of different individuals is collectedwhich is then segmented into different parts which are then fitted with some shape whose pa-rameters are calculated to generate a multidimensional vector altering with according to video.A combination of these gives us the required information.  Other types of approaches includethe Gait Energy Image (GEI) which is the average of silhouette over a gait cycle.

**Model-Based Approach** In this kind of approach specific parameters are identified and matched to get the desired result. It involves identifying mathematical constructs that represent discriminative gait features with some parameters. The parameters are grouped into spatiotemporal and kinematic. Spatio-temporal parameters include the step length and height (stride) speed and gait cycle time while the kinematics include the joint rotations and the angle between different joints. This approach reliably handles the occlusion, noise, scale etc which fails in the case of model-free approaches.

![Figure 1: Model-free and Model-based approaches](/3D-Gait-Recognition/assets/img/post/img1.png)
        *Figure 1: Model-free and Model-based approaches*

# Problem Statement
**3D-Gait-Recognition**  Creating a deep learning pipeline for the identification of the personby the manner of its walking i.e. using his/her gait features.

![Figure 2: Gait Recognition](/3D-Gait-Recognition/assets/img/post/gait.png)
        *Figure 2: Gait Recognition*

## Dataset
The dataset that we will be using in the project will be the   **Human3.6M** dataset. 
The dataset consists of 3.6 million different human poses collected with 4 digital cameras. The data is organized into 15 training motions containing walking with many types of asymmetries (e.g. walking with a hand in a pocket, walking with a bag on the shoulder), sitting and laying down poses, various types of waiting poses and other types of poses. The actors were given detailed tasks with examples in order to help them plan a stable set of poses between repetitions for the creation of training, validation and test sets. In the execution of these tasks the actors were however given quite a bit of freedom in moving naturally over a strict, rigid interpretation of the tasks.

## Edge Device
**Jetson Tx2** : 
Jetson TX2 is the fastest, most power-efficient embedded AI computing device. The latest addition to the industry-leading Jetson embedded platform, this 7.5-watt supercomputer on a module brings true AI computing at the edge. It's built around an NVIDIA Pascal™-family GPU and loaded with 8 GB of memory and 59.7 GB/s of memory bandwidth. It features a variety of standard hardware interfaces that make it easy to integrate it into a wide range of products and form factors.

![Figure 3: Jetson Tx2 Module](/3D-Gait-Recognition/assets/img/post/jetson.jpg)
        *Figure 3: Jetson Tx2 Module*

## Pipeline
Below is the proposed pipeline for the project : 

* Identifying and creating the Ground Truth data.
* Getting the individual poses for each of different concerned 	objects in each frame.(DensePose-RCNN)
* Establishing the spatio-temporal relationships between the frames in the gait cycle using RNNs or LSTMs.
* Optimizing the above network by creating TensorRT engine to work on the Nvidia Jetson Tx2.

# References
1. A. Schrijver,Combinatorial Optimization - Polyhedra and Efficiency. Springer, 2003.
2. R. G. Gallager, “Low density parity check codes,”Transactions of the IRE ProfessionalGroup on Information Theory, vol. IT-8, pp. 21 –28, Jan. 1962.
3. F. Mat ́uˇs, “Infinitely many information inequalities,” inIEEE International Symposium onInformation Theory, (Nice, France), pp. 41 –44, Jun. 2007.
4. Gait recognition - https://www.youtube.com/watch?v=emjpqglx14a.”
5. “https://developer.nvidia.com/embedded/buy/jetson-tx2.”
6. N. N. R. A. Guler and I. Kokkinos,  “Densepose:  Dense human pose   estimation in thewild,” 2018.
7. P. D. K. He, G. Gkioxari and R. G. M, “Mask rcnn,” 2017


**Note**: PDF copy of this report can be found at [here](/3D-Gait-Recognition/reports/interim_progress_report.pdf)
