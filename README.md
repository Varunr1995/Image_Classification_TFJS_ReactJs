# Model Development

Developed two Deep Learning Algorithms, one with basic CNN architecture and other with the trnasfer learning technique

Basic CNN Architecture which is the very first way used for the identification and classification of images.


The main reason to use transfer learning technique for the development of keras model, as the model was already trained on huge datasets. https://paperswithcode.com/media/methods/Screen_Shot_2020-06-12_at_1.24.15_PM_qDb6V3G.png

RestNet is having the advantage of “identity shortcut connection” which means it skips one or mode layers. The reason why skipping happens is, Stacking layers shouldn’t degrade the network performance, because we could simply stack identity mappings (layer that doesn’t do anything) upon the current network, and the resulting architecture would perform the same. This indicates that the deeper model should not produce a training error higher than its shallower counterparts. They hypothesize that letting the stacked layers fit a residual mapping is easier than letting them directly fit the desired underlaying mapping. And the residual block above explicitly allows it to do precisely that. ResNet was not the first to make use of shortcut connections.

# Model Conversion

The model developed by considering the Convolution Layer, Maxpooling Layer, Flatenning, Dense Layer and Dropout will have weights which can be used for future predictions which is otherwise called as transferlearning techniques as this is customised for our realtime usecases. The weights can be stored in few formats, like .pkl and .H5 if we want to connect the model to python web based server. But if we want to use the model in Javascript based web applications, it should need to be converted in to tf.js by using the tf.js library.

The Converted javascript file have weights stored in the form of json which is connected to the javascript webpage, by providing the labels for it aswell.

The weights are already updated in to the ReactJs application, Inorder to alter the weights in the ReactJs just change files in src folder of ReactJs application.

# Requirements

python -m pip install -r requirements.txt 

Inorder to install the Python Libraries used in the development of model.
