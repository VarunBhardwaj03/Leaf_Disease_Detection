# LEAF DISEASE DETECTION MODEL
Identify the type of disease present on a Cassava Leaf image
# Overview
As the second-largest provider of carbohydrates in Africa, cassava is a key food security crop grown by smallholder farmers because it can withstand harsh conditions. At least 80% of household farms in Sub-Saharan Africa grow this starchy root, but viral diseases are major sources of poor yields. With the help of data science, it may be possible to identify common diseases so they can be treated.

Existing methods of disease detection require farmers to solicit the help of government-funded agricultural experts to visually inspect and diagnose the plants. This suffers from being labor-intensive, low-supply and costly. As an added challenge, effective solutions for farmers must perform well under significant constraints, since African farmers may only have access to mobile-quality cameras with low-bandwidth.

In this competition, we introduce a dataset of 21,367 labeled images collected during a regular survey in Uganda. Most images were crowdsourced from farmers taking photos of their gardens, and annotated by experts at the National Crops Resources Research Institute (NaCRRI) in collaboration with the AI lab at Makerere University, Kampala. This is in a format that most realistically represents what farmers would need to diagnose in real life.

Your task is to classify each cassava image into four disease categories or a fifth category indicating a healthy leaf. With your help, farmers may be able to quickly identify diseased plants, potentially saving their crops before they inflict irreparable damage.

Kaggle competition:[Kaggle_competition](https://www.kaggle.com/c/cassava-leaf-disease-classification)


# Brief info about my classification model

I uesd ensemble learning and used transfer learning to predict the output for a given input image. I used MobileNet, ResNet50 & EfficientNetB3 models with pre-trained weights to generate prediction values on the given dataset. I also used data augmentation to make the models more robust using ImageDataGenerator function. 

I used EarlyStopping callback to stop the model from overfitting on training dataset. Also I used ReduceLROnPlateau callback to decrease the learning_rate if the value which is being monitered doesn't changes for a certain number of epochs.

Finally after training all the models for 20 epochs, I got validation accuracy close to 87% for all the models.