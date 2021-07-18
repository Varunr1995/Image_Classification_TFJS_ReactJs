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


# Requirements for ReactJs and Installation Procedure


## Preview

- [Google Play Store](https://play.google.com/store/apps/details?id=YOUR_APP_BUNDLE_ID)
- [App Store]() `Coming soon`

## Technology

- [React](https://reactjs.org/) + [Redux](https://redux.js.org/) + [React Native](https://facebook.github.io/react-native/)
- [React Navigation](https://reactnavigation.org/)
- [Axios](https://github.com/axios/axios)
- [YOUR_OTHER_PACKAGES](https://facebook.github.io/react-native/)

## Requirements

- [Node.js v10+](https://nodejs.org/) + [Yarn](https://yarnpkg.com/)
- [React Native CLI](https://www.npmjs.com/package/react-native-cli) (`npm -g install react-native-cli`)
- [Android Studio](https://developer.android.com/studio/index.html)
- Xcode Command Line tools (`xcode-select --install`)
- [CocoaPods](https://cocoapods.org/) (`gem install cocoapods`)
  More on how to install react native [here](https://reactnative.dev/docs/environment-setup)

## Usage

```sh
# install dependencies
yarn install

# run bundler
yarn run serve

# run on Android device/emulator
yarn run android

# run on iOS device/simulator
yarn run ios

# run tests
yarn run test

# lint code
yarn run lint
```

## Development build

###Android:

```sh
# install dependencies
yarn install

# run bundler
yarn run serve

# Build debug apk
yarn debug-build
```

###iOS

- Run `pod install`
- Switch version to 0.1
- Increment build number
- Archive app
- Sign and upload to TestFlight

## Production build

###Android:

```sh
# install dependencies
yarn install

# run bundler
yarn run serve

#IMPORTANT Before this step increment build number in build.gradle
# Build debug apk
yarn release-build
```

- Upload release-apk to Play Console and wait for review :)

###iOS

- Run `pod install`
- Switch version to 1.0
- Increment build number
- Archive app
- Sign and upload to TestFlight
- After TestFlight is apporved promote release to production
