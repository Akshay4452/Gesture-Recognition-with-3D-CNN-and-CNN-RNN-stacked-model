# Gesture-Recognition-with-3D-CNN-and-CNN-RNN-stacked-model
This is the final project of IIIT-B post Graduate Certification

I have done this with my friend Chandramouli Das.

Gesture Recognition as the name suggests, we had to categorize the gestured provided to the camera. We considered 5 types of gestures in this viz. Thumbs up, thumbs down, swipe left, swipe right, and stop gesture (when use shows his/her palm). The data provided to us was in the form of sequential images in a separate folder and the name of the folder contained gesture type (class label). A CSV file was there which had folder name and gesture type. So the data was not exactly video but a sequence of images (frames).

We built a custom data generator for the data feeding purpose of the model. As this dataset was huge in size we had to build a data generator that would feed the data to the model in steps. Various preprocessing operations were involved in the data generator as you will see in the notebook below. Also, we considered alternate frames of the video so that memory utilization would be less. Image sizes have been resized so that all the images(frames) will be of the same size.

Now comes the model-building part. We have build 2 types of models basically,

3D CNN model
CNN + RNN stacked model
Model iterations are performed by altering hyperparameters and performance is compared for both the models and the best model is selected.

For 3D CNN models, the procedure the straight forward but for CNN + RNN stacked models, it is somewhat tricky. Firstly we have used transfer learning for the CNN layers. We used ResNet50 and ResNet50V2 pre-trained models for transfer learning followed by RNN models like LSTM/GRU. It is advised to use GRU (Gated Recurrent Unit) as it has fewer parameters than LSTM (Long Short Term Memory) and similar accuracy. So we have proceeded with GRU.

As per the project objectives, we were supposed to do the gesture recognition and classification task which we did successfully with good model accuracy. But we think that there is more scope to this project than only gesture recognition.

Future scope: The top-performing model can be implemented in the TV webcam and we can deploy it in real-time to control the TV through gestures instead of remote control by using the interactive web application or mobile app.
