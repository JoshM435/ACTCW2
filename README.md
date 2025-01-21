# ACTCW2 - Machine Learning project involving a dataset.
All of these notebooks were made within Google Colab and function within its system, with the functionality of being able to create tutorial-style notebooks being my main reason for choosing Google colab when making this project.

Python Dependencies;

Q1:So far Kagglehub, os, cv2, numpy, matplotlib.pyplot, google.colab.patches -> cv2_imshow.

Q2:

Q3:

In This project I have chosen a kaggle dataset: Airbus Aircraft Detection. This dataset consists of top-down aerial photos of airports, where buildings, various vehicles, planes, etc are present. In this project i will attempt to use a traditional non-neural network method as well as a neural network method to analyse the photos in the dataset to determine planes present. 
For Q1 and Q2 the aim is make a tutorial style notebook, being aimed towards a Beginner-style audience, with the purpose of highlighting why certain choices were made when developing a solution to the problem. 
For Q1 my problem was to determine the planes present in the images within the kagglehub dataset, with the goal to make the process of counting/identifying planes easier, whilst also making it uneccessary for a human to do the workload of filtering through images and counting the planes one by one. With the overarching aim of using a traditional method and trying to attain a high accuracy of counts.
Whilst also approaching a research problem 'Q3: How does data augmentation affect the performance of a neural network?' alongside my Neural Network and exploring the applicability of my neural network to the problem at hand. It will consist of a tutorial style notebook, with Machine Learning as its central focus, with explanation of the code being used and the choices made when choosing these methods, specifically comparing the affects of data augmentation on the detection process, as well as the counting process.
For Q1: traditional non-neural network method. I used an edge-detection/Contour-analysis approach to attempt to determine the planes present within the datasets images.
