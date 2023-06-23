# Industrial_Motion_Classifier. 
It's classify the motion and vibration data from a stand fan. This is to mimic using embedded machine learning in an industrial environment. We want to be able to determine if a machine is off, on, low, high, anomaly, etc.
1-first of all Make sure that your phone shows up in the Edge Impulse devices list.
2-Attach the phone to the machine as best as you can and leave space so you can access your screen
3-Make sure your phone is connected to your Edge Impulse project by navigating to smartphone.edgeimpulse.com on your phone’s browser.
4-You will need to choose a few classes for your model to be able to predict (for my project: Light, Heavy load, and Off).
5-Head to the Impulse design page in your project. Add a Spectral Analysis processing block. Add a Neural Network block and a K-means Anomaly Detection block to the learning blocks section.
6-Head to the NN Classifier page in your project. Click Start training. After a few minutes, the model should be done training.
7-Go to the Anomaly detection page of your project. Select suggested axes(these will most likely be the RMS values for the X, Y, and Z axes). Click Start training. 
8-Go to the Model testing page in your project. Click the checkbox next to Sample Name to select all of your test samples. Click Classify.
9-In your phone’s browser, head to smartphone.edgeimpulse.com to reconnect the phone to your project. Click the Switch to data collection mode button at the bottom of the page. The phone will automatically have Edge Impulse build your project and download it. From there, it will run locally on your phone’s browser.
10-Take a look at the output of the class predictions.my model has a hard time distinguishing between the light and anomaly classes (just like I saw in the test set). However, it is effective in determining if the fan is on or off.

For now, I’m happy being able to determine if my fan is on, off, or has an anomaly (off-balanced motor or large, heavy object causing odd vibrations). However, if I wanted to create a more accurate classifier, I would need to spend more time tweaking hyperparameters, gathering lots more data 
