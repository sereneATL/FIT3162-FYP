# FIT3162-FYP

## Machine Learning Code Scripts

### 1. Data Query

Contains the code used to query the data from the LIDC dataset, along with resizing and labelling functions.

### 2. ML Preprocessing

Contains all the remaining data preprocessing code. This includes normalization, stacking, resizing and saving the data and labels in a CNN-ready format.

### 3. 2D Vanilla AlexNet Norm 1

Contains the AlexNet training script used on data normalized using technique 1, that is a standard min-max normalization using the minimum and maximum pixel values of the dataset. Training logs and performance metrics are present. 

### 4. 2D Vanilla AlexNet Norm 2

Contains the AlexNet training script used on data normalized using technique 2, that is a min-max normalization using hanpicked values corresponding to the range of pixels with the highest frequency, in an attempt to minimize the impact of outliers. Training logs and performance metrics are present. 

### 5. 2D Optimized AlexNet

Contains the optimized AlexNet training script, used on data normalized using technique 2. Tuning done to increase the performance of AlexNet on the LIDC dataset include:

- Reducing the batch size
- Changing the optimization function from SGD+momentum to Adam
- Consequently, removing L2 regularization
- Changing the learning rate to the Adam standard (0.001)

Training logs and performance metrics are present 

### 6. 3D Vanilla AlexNet

Contains the 3D AlexNet training script, initialized with all the parameter values described in the original AlexNet paper. As can be seen from the training scripts, the CNN has not yet converged by 50 epochs, and further training needs to be done. However, the model is saved after 50 iterations, and performance metrics are present. 

### 7. 3D Optimized AlexNet

Contains the optimized AlexNet training script, used on data normalized using technique 2. Tuning here was done similarly as with the 2D AlexNet, but the dropout was also increased to 0.6. It appears that using Adam in this case has caused a much faster convergence, but the performance of the model remains poorer than the 2D model, possibly due to the training time/performance trade off that comes with using Adam. Training logs and performance metrics are present. 

## 8. ML Testing

Contains simple unit tests of the functions used to preprocess the data. 
