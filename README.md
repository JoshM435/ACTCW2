# ACT CW2 - Machine Learning project involving a dataset.
# UP2066955
All of these notebooks were made within Google Colab and function within its system, with the functionality of being able to create tutorial-style notebooks being my main reason for choosing Google colab when making this project.

Python Dependencies;

Q1:Kagglehub, OpenCV, Matplotlib, NumPy. See Dependencies for versions.
Random, os, ast, Do not have versions in Colab.

Q2:Kagglehub, pandas, TensorFlow, Matplotlib, Torch, Torchvision, NumPy, Pillow (PIL). See Dependencies for versions.
Random, os, ast do not have versions in Colab.

Q3:Kagglehib, pandas, TensorFlow, PyTorch, Torchvision, Matplotlib, Pillow (PIL), NumPy. See Dependencies for versions. 
Random, os, ast do not have versions in Colab.

In This project I have chosen a kaggle dataset: Airbus Aircraft Detection. This dataset consists of top-down aerial photos of airports, where buildings, various vehicles, planes, etc are present. In this project i will attempt to use a traditional non-neural network method as well as a neural network method to analyse the photos in the dataset to determine planes present. 

The Kaggle Dataset: Airbus Aircraft Detection allows for the testing of a multitude of detection software/methods, it is made up of High Resolution Satellite imagery. It's purpose is to train models to provide information about activity regarding any airport, with the size, number and type of aircraft not being limiting factors.

For Q1 and Q2 the aim is make a tutorial style notebook, being aimed towards a Beginner-style audience, with the purpose of highlighting why certain choices were made when developing a solution to the problem. 

For Q1 my problem was to determine the planes present in the images within the kagglehub dataset, with the goal to make the process of counting/identifying planes easier, whilst also making it uneccessary for a human to do the workload of filtering through images and counting the planes one by one. With the overarching aim of using a traditional method and trying to attain a high accuracy of counts.

Whilst also approaching a research problem 'Q3: How does data augmentation affect the performance of a neural network?' alongside my Neural Network and exploring the applicability of my neural network to the problem at hand. It will consist of a tutorial style notebook, with Machine Learning as its central focus, with explanation of the code being used and the choices made when choosing these methods, specifically comparing the affects of data augmentation on the detection process, as well as the counting process.

For Q1: traditional non-neural network method. I used an edge-detection/Contour-analysis approach to attempt to determine the planes present within the datasets images. This notebook can be ran in Google Colab, cell by cell. This method is very simple and the detection is based off edges detected after grayscaling an image and retaining the data points which correlate to white when shifting to a binary image. The detection is easily skewed from colour variety, shadows, clouds and white buildings.

For Q2: Neural Network approach. I used a Faster R-CNN model which is used for feature detection, and in turn quite useful for this dataset of airport images. This notebook can be ran in Google Colab, with a recommendation for a GPU runtime to be selected, where the notebook can be fully ran from the start with Run All. My approach first had to filter the annotations file and extract the bounding boxes out of their form of 5 tuples into a set of 4 coordinates made up of x_min, y_min, x_max and y_max. A Dataset class would be set up, which would be used to train the model and plot a loss curve, after the training process i test the model on the training set, and then on the extra images provided with the dataset detailing images from both sets of images, with the extra image having predicted bounding boxes plotted on them based off the models training. After which i test for precision in comparison to the ground truth.

For Q3: How does Data Augmentation affect Neural Networks? I chose this approach for my research question as data augmentation on images is visual and it is easy to see the outcome of the training process on the images. With my approach i made three functions which either flip or rotate the image, they are called within an augmentation pipeline class, where it is down to a random number generation whether or not which function gets used, allowing for variety within the augmented dataset. After executing this method it was shown that my data augmentation process negatively effected the training process of the model, despite this the model was able to identify the majority of planes within the dataset, as well as the planes present in the extra images folder within the dataset. 

Despite this outcome, the upsides of Data Augmentation allow for variety in datasets, and expansion of smaller datasets.
