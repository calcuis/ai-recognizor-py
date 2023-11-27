## ai recognizor

This Python code defines a simple graphical user interface (GUI) application for image classification using a pre-trained convolutional neural network (CNN) model. The code utilizes the `taipy.gui` library for GUI components, PIL (Pillow) for image processing, and tensorflow for loading a pre-trained image classification model.

Here's a breakdown of the code:

Import necessary libraries:
- Gui from `taipy.gui` for creating the GUI.
- Image from PIL for working with images.
- `tensorflow` for loading and using a pre-trained neural network model.
- `numpy` for numerical operations.

Define a dictionary `class_names` mapping class indices to corresponding class labels.

Load a pre-trained neural network model using TensorFlow's Keras API. The model is loaded from a file named "baseline.keras."

Define a function `predict_image` that takes the loaded model and the path to an image as input, processes the image, and returns the top probability and predicted class label.

Set up initial variables (`content`, `img_path`, `prob`, `pred`) and define an HTML-like string index, which represents the structure of the GUI. It includes a file selector, an image display, a probability indicator, and a text field for displaying the predicted class.

Define a callback function `on_change` that is triggered when the selected image changes. This function uses the `predict_image` function to obtain the prediction results and updates the GUI state accordingly.

Create a GUI application (Gui object) with the specified structure (`index`) and set the on_change function as the callback for changes in the file selector.

Run the GUI application when the script is executed directly (`__name__ == "__main__"`). The application allows users to select an image file, displays the selected image, and provides a prediction of the image class along with the probability.

Note: The GUI structure (`index`) is defined using a custom syntax (`<|...|>`) provided by the taipy.gui library. The `app.run`(`use_reloader=True`) line runs the GUI application, and `use_reloader=True` enables automatic reloading of the application when the source code changes.
