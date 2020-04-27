# Identifying Graffiti Artwork using Deep Learning

*click on the G icon to view presentation video [![Mock up app icon](/images/G4.jpeg)](https://youtu.be/txwfqmuV4MQ)

[👉 Link to Presentation slides](https://docs.google.com/presentation/d/1pV53Yb_4DMiDk8K0tzbnd-Cba619UyFFFWyFevzH5O4/edit?usp=sharing)

## Motivation
Lower East Side (LES) NYC has been my home for most of my adult life. What makes LES an interesting place to live is the abundance of graffiti artwork which gives the neighborhood a gritty, youthful and hip vibe. I enjoy strolling through my neighborhood and taking pictures of the wide range of graffiti styles. During one of those walks, I wondered how computer vision and machine learning techniques can help to classify graffiti artwork and enable me to learn more about the artists. 

## Objective
Using Keras library utilities, apply transfer learning via pre-trained VGG16 convolutional Neural Network model to classify artwork from 16 graffiti artists.
Train a model that predicts the artist based on unseen graffiti samples.

## Methodology
The 4 main steps of this project were: 
- Perform feature extraction by leveraging a pre-trained convolution base of VGG16 model. 
- Feed the extracted features to a densely connected classifier to get accuracy results for a base model.
- Fine tune the model by making adjustments to the dense units, dropout rate and adding more dense layers to improve the training, validation and test accuracy. 
- Apply data augmentation to help against overfitting.


## Results
### Top-1 Accuracy
The best Top-1 accuracy score was 55% for the baseline model. The configurations for the base line model is as follows: 
- No image augmentation
- 2 Dense Layers
- Batch size = 20
- Drop out = 0.5
- RMSprop Optimizer

The following hyperparameters tuning did not improve the Top-1 Test accuracy score from the baseline model.
- Dense units of 128, dense units of 512
- Drop out of 0.25, drop out of 0.60
- Optimizer Adam, SGD
- Adding a dense layer

### Top-3 Accuracy
A more realistic and effective performance metric to use for this classification problem is Top-3 Accuracy. The baseline model predictions falls in the top three values 77% of the time.

### Confusion Matrix
The confusion matrix not only helped to easily see where the model was right and wrong but it gave insight into the relationship between various artists. 
- It's clear as to why the model did a good job of correctly predicting for the artists Daim, Keith Haring, Retna and Roa. All four artists style of art is singular whether it's all wild animals for Roa, Keith Haring's mostly bold outlines of figures or only bold hieroglyphs and calligraphy by Retna. 
- The model was understandably mixed up between Banksy and Ble le Rat. Further investigation revealed that Banksy was inspired by Blek le Rat and thus both share visual similarity to their pieces. 
- The model completely misclassified Futura2000 due to his wide ranging art style.


## Conclusion
In-spite of having a small dataset and large number of classes, the model worked well to understand the stylistic patterns associated with the 16 artists. What I learned from optimization of the model are:
- Too few dense units while low in complexity results in lower accuracy and shows under-fitting while higher dense units with greater complexity but more overfitting and was no better than baseline model of 256 units.
- A small value of dropout regularization does not improve from the baseline accuracy. This is probably due to hidden layers depending a lot on particular features and overfitting or too high drop out results in under-learning.  
- RMSProp and Adam had similar accuracy scores whereas SGD performed poorly.
- Adding dense layers gave the worst accuracy score. With a small dataset, adding additional layers increases complexity and overfits.

## Acknowledgments

- The artwork images were scrapped by using URL links from https://github.com/rememberlenny/graffiti-net/tree/master/_urls .
- This project uses approaches and tools from Chapter 5, section 3 of Francois Chollet "Deep Learning with Python".
- Major thanks goes to Joe Eddy, Kim Fessel and Vinny Senguttuvan for their guidance.
- The G4 icon image was obtained from google search.




