# PawVision: CNN-Powered Image Recognition Model

PawVision is a convolutional neural network (CNN) model designed to classify images of cats and dogs. Using TensorFlow and Keras, the project implements a robust image classification pipeline, showcasing the power of deep learning in computer vision tasks.

## Dataset

The dataset consists of images of cats and dogs, split into training and test sets. The training set contains various augmented images to increase diversity and robustness, while the test set is used for model evaluation.

- **Training Set**: Images are rescaled, sheared, zoomed, and horizontally flipped to prevent overfitting.
- **Test Set**: Images are rescaled to ensure consistency with the training data.

## Project Structure

### 1. Data Preprocessing

- **Training Set Augmentation**: Applied feature scaling, shear, zoom, and horizontal flip.
- **Test Set Preprocessing**: Applied feature scaling.

### 2. Building the CNN

- **Initialization**: Created a sequential model.
- **Convolutional Layers**: 
  - Added two Conv2D layers with ReLU activation.
  - Max-pooling layers to reduce dimensionality.
- **Flattening**: Converted feature maps into a 1D vector.
- **Fully Connected Layer**: Dense layer with 128 units and ReLU activation.
- **Output Layer**: Dense layer with a sigmoid activation for binary classification.

### 3. Training the CNN

- **Compilation**: Used Adam optimizer and binary cross-entropy loss.
- **Training**: Trained for 25 epochs on the training set with evaluation on the test set.

### 4. Making Predictions

- Loaded and preprocessed single images for prediction.
- Output whether the image is of a cat or dog.

## Results

The model achieved an accuracy of **90.81%** on the test set with a final loss of **0.2317**. While the results are promising, there are several ways to potentially improve the model's performance:

1. **Data Augmentation**: Experiment with additional augmentation techniques or parameters.
2. **Model Architecture**: Increase the depth of the network or add more filters.
3. **Regularization**: Implement dropout or L2 regularization to reduce overfitting.
4. **Learning Rate Adjustments**: Use learning rate schedules for better convergence.
5. **Batch Normalization**: Add batch normalization layers to stabilize training.


## Conclusion

This project showcases the implementation of an Convolutional Neural Network (CNN) model designed to recognize images of cats and dogs. With further enhancements and more complex architectures, the model's performance can potentially be improved.

## How to Run

1. Clone the repository.
2. Install the required libraries from `requirements.txt`.
3. Run the Jupyter notebook to preprocess data, build, train, and evaluate the CNN model.

----