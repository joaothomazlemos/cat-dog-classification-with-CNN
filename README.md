# Cat and dog classification with Convolutional Neural Network
Master's assigment done in 2021

# Objective
Train a convolutional neural network to predict images classified in dogs or cats.

# Training and test data info:

The dataset used has 25000 labeled images, of which 4000 were used, 80% for training and 20% for validation.

# Discussion and results:

The neural network was initially fed with the same number of samples and the same height and width in relation to the other models. However, the neural network needs a very large set of samples, and it also needs the samples to have high resolution compared to other models, so that it can make coherent predictions. It was possible to see this in practice, since with little data the network could not generalize so well, memorizing the set and overfitting, which generated random predictions. Furthermore, the network happened to memorize only one class, having a prediction of approximately 50%. It was later noticed, by the confusion matrix, that the reason was that the network got everything right from just one class, naturally, because any image it judged would be associated with only one of the classes, and there was a balance of the data, where 50% of the set belonged to each of the classes. In addition to increasing the number of images, the image augmentation technique was used, so that each time the network saw a batch of images pass through the iteration (epoch), the image was never the same, since it could have a different scale. , rotation, height offset, width offset, and mirroring. Also, the dropout method was used, so that the neurons were randomly deactivated at each iteration, so that the influence of a given weight would not overshadow the others in a dominant way, which generated less biases and increased generalization. After these modifications, a good result was obtained, as expected from neural networks, which are widely used for tasks related to computer vision, mainly in object detection. The accuracy of the model was high as expected, at 82% accuracy.
