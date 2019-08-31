## A-custom-image-classifier-using-TensorFlow.js
A custom image classifier that i will train on the fly in the browser using TensorFlow.js, a powerful and flexible machine learning library for Javascript. 

I will first load and run a popular pre-trained model called MobileNet for image classification in the browser. 

I will then use a technique called "transfer learning", which bootstraps our training with the pre-trained MobileNet model and customizes it to train for my application.

We will make a custom 4-class object classifier using the webcam on the fly. We're going to make a classification through MobileNet, but this time we will take an internal representation (activation) of the model for a particular webcam image and use that for classification.

We'll use a module called a "K-Nearest Neighbors Classifier", which effectively lets us put webcam images (actually, their MobileNet activations) into different categories (or "classes"), and when the user asks to make a prediction we simply choose the class that has the most similar activation to the one we are making a prediction for.

Now when we load the index.html page, we can use common objects or face/body gestures to capture images for each of the three classes. Each time we click one of the "Add" buttons, one image is added to that class as a training example. While we do this, the model continues to make predictions on webcam images coming in and shows the results in real-time.


## What we'll learn
1.How to load pretrained MobileNet model and make a prediction on new data
2.How to make predictions through the webcam
3.How to use intermediate activations of MobileNet to do transfer learning on a new set of classes you define on the fly with the webcam
