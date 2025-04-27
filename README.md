readme_text = """
# Cloud Image Classification using Deep Residual Networks

## Project Description

This project focuses on classifying cloud images into 11 different categories using a custom-built Deep Residual Network (DeepResNet) model. The project demonstrates the effectiveness of deep networks with residual connections for image classification tasks, particularly how they can improve performance compared to simpler Convolutional Neural Networks (CNNs).

Key features of this project include:

* **Custom DeepResNet Model:** A deep network architecture composed of Residual Blocks and Max Pooling layers for enhanced feature extraction and gradient flow.
* **Data Augmentation:** Implementation of data augmentation techniques (Random Horizontal Flip, Random Rotation, and Color Jitter) to increase the diversity of the training data and improve the model's generalization ability, reducing overfitting.
* **Learning Rate Scheduling:** Utilization of a CosineAnnealingLR scheduler to dynamically adjust the learning rate during training, leading to faster convergence and potentially better model performance.
* **Exploration of Deep Networks:** Investigation into how increasing the depth of the network using residual connections impacts the classification performance.

## Model Choice

We designed a custom **DeepResNet** model for this project. The choice of a DeepResNet is motivated by its ability to:

* **Go Deeper:** Residual connections address the vanishing gradient problem, allowing the creation of much deeper networks than traditional CNNs.
* **Maintain Gradient Flow:** The skip connections in Residual Blocks facilitate the direct flow of gradients, ensuring that even in very deep networks, the gradients remain strong enough to update the weights effectively.
* **Improve Performance:** Deeper networks often have a higher capacity to learn complex features, leading to improved classification accuracy compared to basic CNN models.

## Dataset

The dataset used for this project contains cloud images categorized into 11 distinct classes.

**Dataset Link:** [https://drive.google.com/drive/folders/1BpKfJDQMSM8d9mL16VoZwkRb26H82CoZ?usp=sharing](https://drive.google.com/drive/folders/1BpKfJDQMSM8d9mL16VoZwkRb26H82CoZ?usp=sharing)

**Instructions to Use the Dataset:**

1.  Download the dataset from the provided Google Drive link.
2.  Extract the downloaded zipped file.
3.  Place the extracted `Cloud` folder in the following path within your Google Drive (assuming you are using Google Colab as in the provided "How to Run" instructions):
    ```
    /content/drive/MyDrive/Cloud
    ```
    Ensure that the `training` directory, containing the 11 class subfolders, is located at `/content/drive/MyDrive/Cloud/training/`.

## Installation

To run this project, you need to have the following libraries installed. You can install them using `pip`:

```bash
pip install torch torchvision scikit-learn matplotlib tqdm
