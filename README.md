# Identifying Graffiti Artwork using Deep Learning
*click on G icon to view presentation video
[![Mock up app icon](/images/G4.jpeg)](https://youtu.be/txwfqmuV4MQ)

[👉 Link to Presentation slides](https://docs.google.com/presentation/d/1pV53Yb_4DMiDk8K0tzbnd-Cba619UyFFFWyFevzH5O4/edit?usp=sharing)
## Motivation


## Objective
Using Keras library utilities, applied transfer learning via pre-trained VGG16 convolutional Neural Network model to classify artwork from 16 graffiti artists.
Train a model that predicts the artist based on an unseen sample graffiti artwork.
## Methodology



## Results
### Top-1 Accuracy
The best Top-1 accuracy score was 0.55 for the baseline model. The configurations for the base line model is as follows: 
- No image augmentation
- 2 Dense Layers
- batch size = 20
- Drop out = 0.5
- RMSprop Optimizer

The following hyperparameters tunning did not improve the Top-1 Test accuracy score of the baseline model.
- Dense units of 128, dense units of 512
- Drop out of 0.25, drop out of 0.60
- Optimizer Adam and SGD
- Adding a dense layer

### Top-3 Accuracy
A more realistic performance metric to consider is Top-3 Accuracy for the baseline model. The Top-3 Accuracy result was 0.77. 

### Confusion Matrix
The confusion matrix 

## Acknowledgments

1. The artwork images were scrapped by using URL links from https://github.com/rememberlenny/graffiti-net/tree/master/_urls .
2. This project uses approaches and tools from Chapter 5, section 3 of Francois Chollet "Deep Learning with Python".
3. The G4 icon image was obtained from google search.




