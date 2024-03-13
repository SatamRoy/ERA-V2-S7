# ERA-V2-S7
CNN for MNIST image classification
We are constructing a Convolutional Neural Network (CNN) model specifically for MNIST image classification. Our approach is modular, beginning with a foundational codebase and progressively enhancing it to achieve an impressive 99.40% testing accuracy within 15 epochs.

**Basic Working Model**: Constructing a foundational model with the correct structure, ensuring essential components are in place.

**Complexity Reduction Model**: Refining architecture to reduce complexity.

**Lightweight Model**: Exploring lightweight strategies, aiming for efficiency without compromising accuracy.

**Final Model**: Pushing boundaries with < 8000 parameters, while still achieving our 99.40% accuracy target.
We are building 4 models here. 

# Model_1: (Basic Working Model)
## Building a basic Model for MNIST Image Classification
###Targets:
Getting the correct set-up
Adding basic transformers and data loaders
Setting up basic training and testing loop

### Result
* **Total number of parameters**: 194.8 k
* **Best Training Accuracy**: 99.21 (at 15th Epoch)
* **Best Test Accuracy**: 99.05 (at 15th Epoch)
### Analysis
* **Both training and testing accuracies are very high** (more than 99%), which indicates that the model is capable of learning the patterns in the data effectively
* The training accuracy is higher than the testing accuracy --> this suggests that the model might be **overfitting the training data**
* To improve generalization, we will consider techniques like **regularization, dropout in the next model**

# Model_2: (Complexity Reduction Model)
##Building a simplified model with batch normalization and Regularization
### Targets:
* Making a lighter Model
* Adding batch normalization to increase accuracy
* Adding drop-out layer to make the training harder and to improve generalization



# Model_3: (Lightweight Model)
## Build an even lighter model
### Target
* Remove the last layer with Global Average Pooling layer
### Result
* **Total number of parameters**: 5.5 k
* **Best Training Accuracy**: 98.27%
* **Best Test Accuracy**:98.79%
### Analysis
* The models **training accuracy has been stagnated** at around 98.15 - 98.27%. As this is not increasing, we understand that we need to increase the complexity of the model.
* Test accuracy is little higher than training accuracy, which means the model is **not overfitting**.

# Model_4: (Final ModelFinal Model)
## Build a model to achieve more than 99.40% test accuracy
### Targets
* **Number of Parameters**: Less than 8 k
* **Image Augmentation** to increases the diversity of the dataset and the robustness of the model
* Added **Learning rate schedular** faster convergence
* And Finally to get more than **99.40% test accuracy** in approximately 15 epochs
### Result
* **Total number of parameters**: 7.6 k
* **Best Training Accuracy**: 99.47%
* **Best Test Accuracy**: 99.50%
### Analysis
* Both training and testing accuracies are very high (more than 99.47%), which indicates that the **model is capable of learning the patterns** in the data effectively
* Since the test accuracy is very close to the training accuracy, it seems that the model is **not significantly overfitting or underfitting** --> There is no significant gap between training and test accuracy, which is a positive sign
* The close alignment of **training and test accuracy suggests a reasonable fit**
