# Artistic Style Transfer

## Overview
This project aims to create a deep learning model for artistic style transfer, allowing the adaptation of an original artwork to resemble the aesthetic of any chosen art. The model utilizes the InceptionV3 architecture as a backbone to analyze the artistic style of a selected art piece and apply similar stylistic features to a new, original artwork. The result is a piece that appears as though it could have been created by the artist themselves.

## Methodology
1. Dataset Preparation
  - Two images are required for the style transfer process: a content image (the original artwork to be transformed) and a style image (the reference artwork whose style will be applied).

2. Feature Extraction
  - The InceptionV3 model is used as a feature extractor. The chosen content layer is 'conv2d_93', and five style layers are selected: 'conv2d', 'conv2d_1', 'conv2d_2', 'conv2d_3', and 'conv2d_4'.
  - The content and style layers are combined into a list for further processing.

3. Style Transfer
  - The project defines functions for style and content loss calculations, as well as a function to calculate the Gram matrix. These functions are crucial for quantifying the stylistic and content differences between the images.
  - The model optimizes a generated image to minimize the combined style and content loss, effectively transferring the style of the reference image to the content image.

4. Training the Model
  - The style transfer process is initiated by calling the fit_style_transfer function, specifying parameters such as style and content weight, optimizer, epochs, and steps per epoch.
  - The model iteratively updates the generated image to minimize the defined loss function.

## Usage
  - Set the paths for the content and style images in the provided code.
  - Run the notebook to load and preprocess the images, build the feature extractor, and perform style transfer.
  - Adjust parameters such as style and content weight, optimizer, epochs, and steps per epoch as needed.
  - Analyze the stylized images generated during the training process.

## Results
  - The final stylized image is obtained after the specified number of epochs.
  - Visualizations of the stylized images at different steps are available for analysis.

## Dependencies
  - TensorFlow
  - Keras
  - Matplotlib
  - NumPy
  - ImageIO
