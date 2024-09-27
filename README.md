# Convolutional Neural Network (CNN) - Cat and Dog Image Classifier
Computer Vision project using **TensorFlow** and **Keras** under freeCodeCamp's Machine Learning with Python curriculum

The dataset is provided by [freeCodeCamp](https://cdn.freecodecamp.org/project-data/cats-and-dogs/cats_and_dogs.zip)

The Jupyter Notebook is stored in project_fcc_cat_dog.ipynb


### 1. Description of the dataset used

<pre>
The structure of the dataset files:
cats_and_dogs
|__ train:
    |______ cats: [cat.0.jpg, cat.1.jpg ...]
    |______ dogs: [dog.0.jpg, dog.1.jpg ...]
|__ validation:
    |______ cats: [cat.2000.jpg, cat.2001.jpg ...]
    |______ dogs: [dog.2000.jpg, dog.2001.jpg ...]
|__ test: [1.jpg, 2.jpg ...]<br>
</pre>


### 2. Details of the preprocessing steps

The images are labeled with "dogs" and "cats" in train and validation datasets, while images in test dataset is not labelled.

First, the images in train and validation datasets are decoded into floating tensors and rescaled betwwen 0 and 1.

Then, more training data is create from existing training examples by using random transformations.

After that, a convolution neural network model is created and compiled with Conv2D, MaxPooling2D, Dropout, Flatten and Dense layers.

Next, the model is trained and plots of the loss and accuracy on the training and validation sets were observed for model evaluation.

![model evaluation](https://github.com/user-attachments/assets/11b5de5b-8220-4084-b1e1-b407cbebcf23)

Finally, the test images are fit to the model for cats and dogs prediction.

<br>
  
### 3. Evaluation of results

Examples of plots of the images in the test sets with the probability confidence:

![prediction](https://github.com/user-attachments/assets/067c1d77-80d5-4303-b00d-124438555005)

Ground truth check:

![result](https://github.com/user-attachments/assets/f05a824a-966a-418f-9c72-61f687426c75)

<br>

### 4. Insights into the model's limitations

First, the coreect percentage of classification is around 68%, which is still low of confidence in classifying cats and dogs.

Second, the model consists of more than 9.5 millions parameters and it requires a huge computational power for training. Howerever, the training process and be speeded up by using GPUs or TPUs.

<br>

### Credits 

Author: Bobby
