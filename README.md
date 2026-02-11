<!-- This is the markdown template for the final project of the Building AI course, 
created by Reaktor Innovations and University of Helsinki. 
Copy the template, paste it to your GitHub README and edit! -->

# SmartBin AI

Final project for the Building AI course

## Summary

SmartBin AI is a simple AI-based image recognition concept that helps people sort their waste correctly. The system uses image classification to identify whether an item belongs to bio waste, plastic, paper, metal, or mixed waste, helping reduce recycling mistakes.

Building AI course project


## Background

Many people are unsure how to sort their waste correctly. Recycling rules vary, and mistakes are common.

Which problems does your idea solve?

* People do not know which bin to use
* Recycling instructions are confusing
* Wrong sorting increases environmental waste
* Recycling contamination causes extra processing costs

This problem is common in households, schools, and workplaces. Incorrect recycling reduces the effectiveness of environmental efforts. A simple AI assistant could make sorting easier and more accurate.


## How is it used?

The user opens a mobile application and takes a picture of an item (for example, a yogurt container or coffee cup).

The AI system:

* Identifies the object in the image
* Classifies it into a waste category
* Provides short sorting instructions

The solution is mainly used at home, in schools, and in public recycling areas. It should be fast and easy to use in everyday situations.

![Recycling](https://upload.wikimedia.org/wikipedia/commons/4/4c/Recycling_bins.jpg)
```
from tensorflow.keras.applications import MobileNetV2
from tensorflow.keras.preprocessing import image
import numpy as np

model = MobileNetV2(weights='imagenet')

img = image.load_img('example.jpg', target_size=(224, 224))
img_array = image.img_to_array(img)
img_array = np.expand_dims(img_array, axis=0)

predictions = model.predict(img_array)
print("Prediction:", predictions)
```


## Data sources and AI methods

Where does your data come from?

* Public image datasets of household waste
* Open image classification datasets
* User-submitted labeled images

AI methods used:

* Convolutional Neural Networks (CNN)
* Transfer learning (e.g., MobileNet)
* Supervised learning

| Method | Description |
|--------|------------|
| CNN | Image classification |
| Transfer learning | Uses pre-trained model |
| Supervised learning | Training with labeled data |


## Challenges

What does your project not solve?

* Local recycling rule differences
* Extremely ambiguous waste items
* Dirty or damaged objects

Limitations and ethical considerations:

* Image recognition is not always 100% accurate
* The system must clearly state that results are recommendations
* Data privacy must be respected if users upload images


## What next?

How could your project grow?

* Location-based recycling rules
* Integration with smart trash bins
* Gamification features
* Larger custom-trained dataset

To develop this further, programming skills, labeled datasets, and real-world testing would be needed.


## Acknowledgments

* Building AI course by University of Helsinki & Reaktor
* Concept inspired by environmental sustainability initiatives
* Example code adapted from TensorFlow documentation



