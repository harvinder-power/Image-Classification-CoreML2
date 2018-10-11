# Image Classification with CoreML2 for iOS
## Introduction
With the advent of CoreML2 for iOS, Machine Learning has become more accessible, with simple models easily trainable on most laptops. This project demonstrates a simple modification of the model to be targeted towards diagnosis of pneumonia on a chest x-ray.

## Initialisation
To start this project, open the `ChestXray.xcodeproj` file using XCode.
*Note - this will require MacOS Mojave to be installed with the latest version of XCode, else CoreML will fail to run.*

## Training a model
To train your own model - this can be done in XCode Playgrounds. Start a new Playground and run the following code to bring up a live view of the ML builder.

```swift
import CreateMLUI

let builder = MLImageClassifierBuilder()

builder.showInLiveView()
```

## Changing the model
The model used can be easily changed for another with a simple modification to the code. In `ImageClassificationViewController.swift` change `let model = try VNCoreModel(for: Pneumonia().model)` with Pneumonia() being substituted for your model name. Ensure that your package is appropriately signed to prevent warnings and build-time errors.

## Next Steps
- Re-training the model (at present, issues exist with overfitting of the model), and broaden the scope to a larger range of conditions.
- Allow for a more user friendly UI with visualisation of previous analyses.
