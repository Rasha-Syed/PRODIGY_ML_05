# Task 05: Food Item Recognition with ResNet50

## Objective
Develop a model that can accurately recognize food items from images.

### Dataset
- **food-101/images/**: Contains images organized in subfolders by food categories.
- **food-101/meta/classes.txt**: Contains class labels corresponding to the food categories.
- **food-101/meta/train.txt**: Lists the training image file paths.
- **food-101/meta/test.txt**: Lists the test image file paths.

  **Dataset Link**: https://www.kaggle.com/dansbecker/food-101

#### Steps Implemented

##### Data Preparation
- **Created a balanced subset of the dataset** to ensure manageable training size and class representation.
- **Applied data augmentation techniques** such as horizontal flipping, zooming, and rotation to enhance the model’s robustness.

##### Data Loading and Preprocessing
- **Loaded images and labels using TensorFlow’s `ImageDataGenerator`** to prepare training and validation datasets.
- **Resized images to 100x100 pixels** for consistent input size to the model.

##### Model Building
- **Utilized ResNet50 with transfer learning** to leverage pre-trained weights for effective image classification.
- **Added custom classification layers** on top of the ResNet50 base model to adapt it for the specific food classification task.

##### Model Training
- **Compiled the model using the Adam optimizer** and categorical cross-entropy loss function.
- **Trained the model with a learning rate scheduler** to adjust the learning rate based on validation loss.

##### Model Evaluation
- **Evaluated model performance** on the validation set using accuracy metrics.
- **Visualized predictions** by comparing predicted and actual labels for a sample of images.

##### Visualization
- **Displayed sample images alongside predictions and actual labels** to assess model performance visually.
- **Plotted training and validation accuracy and loss curves** to analyze the model’s learning progress over epochs.

### Model Evaluation Metrics
- **Validation Accuracy**: Accuracy of the model on the validation dataset.
- **Visualization Results**: Side-by-side comparison of predicted vs actual labels for sample images.

### Files Included
- **food-101/images/**: Directory with food images organized by class.
- **food-101/meta/classes.txt**: File containing food class labels.
- **food-101/meta/train.txt**: File listing training image paths.
- **food-101/meta/test.txt**: File listing test image paths.

### Requirements
- **Python 3.x**
- **TensorFlow 2.x**
- **Keras**
- **NumPy**
- **Matplotlib**
- **Pandas**
