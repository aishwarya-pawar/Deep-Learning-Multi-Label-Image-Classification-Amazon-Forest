# Understanding-the-Amazon-from-Space
### Our solution to Planet's kaggle challenge to track human footprint in Amazon rainforest using deep learning.
The Amazon is home to one million indigenous people and three million species of plants and animals. It is essential to pinpont the location of deforestation and human encroachment to enable speedy response times and curb further damage to the ecosystem. Advancement in satellite imagery coupled with machine learning has paved way for detecting small-scale deforestation and differentiating between human and natural causes of deforestation.

### The Team
Aishwarya Pawar, Ananya Garg, Onyekachi Ugo, Sachin Balakrishnan and Sahana Subramanian from The University of Texas at Austin. For the complete review of the project-work, please find our blog post -

### Overview
We have a multilabel image classification problem in hand, with every image linked to one or more of the 17 ground/atmospheric conditions, land cover and land use. We used Tensorflow, Keras and scikit-learn to develop the CNN models. There are 8 jupyter notebooks in this repo and each one of these corresponds to specific models or functions which we came up with to tackle this tough competition.

### Steps and Repo structure:
CNN.ipynb : A CNN we built from scratch to start off with.

Amazon - APM - XGBoost.ipynb : XG Boost to evaluate the model performance on rare labels.

ResNet - APM - Amazon- vff.ipynb : Transfer learning with Keras ResNet model.

VGG16.ipynb : Transfer learning with Keras VGG16 model.

MobileNet - CV.ipynb : Transfer learning with Keras MobileNet.

Haze Removal - Model.ipynb : Image pre-processing with Haze Removal algorithm.

Rare label detection model.ipynb : Additional model to detect Rare labels in the input data.

Ensemble.ipynb : Final Ensemble.

### Challenges and Results
The biggest challenge we faced in this project was in dealing with imbalanced classes. Even though this sounds cliché, we would like to highlight the heavy class imbalance in our dataset - with the rarest class representing just around 0.2% of the train data. To tackle this, we trained an additional CNN model solely for rare label detection and had done advanced pre-processing with Haze removal.

The pretrained CNN models are really powerful, so you might hit the baseline accuracy most of the time. To boost the model performance beyond this, you will need proper hyperparameter tuning and understanding of the areas that need additional investigation. With the extra pre-processing and model development( for rare labels), we could achieve a significant lift in the rare label F1 scores. As the final step, we ensembled multiple deep learning models and got to our final kaggle f-beta score of 0.927521.
