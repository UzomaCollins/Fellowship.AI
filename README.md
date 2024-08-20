# Fellowship.AI
Computer Vision Challenge: Training ResNet-50 on the Flowers Dataset

Overview
This is a 102 category dataset, consisting of 102 flower categories. The flowers chosen to be flower commonly occuring in the United Kingdom. Each class consists of between 40 and 258 images. The images have large scale, pose and light variations. In addition, there are categories that have large variations within the category and several very similar categories.

The challenge involves working with a Computer Vision (CV) task where i used a pre-trained ResNet-50 model to train on the Flowers dataset.

Key Concepts
1. ResNet-50
ResNet-50 is a deep convolutional neural network (CNN) architecture with 50 layers.
It's known for its ability to learn deep features from images, making it very effective for image classification tasks.
ResNet-50 is pre-trained on a large dataset like ImageNet, meaning it already has learned useful features from millions of images.
2. Pre-trained Model
A pre-trained model has already been trained on a large dataset and can be fine-tuned for specific tasks.
Fine-tuning a pre-trained model on a new dataset often leads to better performance and faster training compared to training a model from scratch.
3. Flowers Dataset
This dataset typically consists of images of different types of flowers.
The goal is usually to classify images into different flower categories.


Challenge Breakdown
1. Load the Pre-trained ResNet-50
I imported the ResNet-50 model with pre-trained weights.
The model is typically pre-trained on ImageNet, which has 1,000 classes.
2. Modify the Model
Since ResNet-50 is pre-trained on ImageNet, we need to modify the last layer to match the number of classes in the Flowers dataset (e.g., 5 classes if there are 5 types of flowers, in this case we have 102 clases).
I replace the final fully connected layer to output the correct number of classes(102).
3. Train the Model on the Flowers Dataset
I fine-tuned the model by training it on the Flowers dataset.
I used the features learned by ResNet-50 and adjusted them to better fit the specific characteristics of the flowers in the new dataset.
4. Evaluate the Model
After training, i evaluate the model’s performance on a test set to see how well it classifies the flowers.

Steps to Implement
Data Preprocessing:
Load and preprocess the Flowers dataset (e.g., resizing images, normalizing pixel values).
Load and Modify ResNet-50:

Load the pre-trained ResNet-50 model.
Modify the final layer to match the number of classes in the Flowers dataset.
Fine-tune the Model:

Train the model on the Flowers dataset.
Optionally, freeze the earlier layers of ResNet-50 to retain their pre-learned features and only train the modified layers.
Evaluate:

Test the model on unseen data and evaluate its performance.
