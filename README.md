# Neural Style Transfer with TensorFlow
Neural Style Transfer (NST) is an optimization technique used to modify the content of an image in the style of another image. This project implements NST using TensorFlow and the VGG-19 model.

## Overview
The project uses the VGG-19 model, a pre-trained deep convolutional neural network, to extract features from the content and style images. The generated image is then optimized to minimize the difference in content and style features from the respective images.

## Key Concepts
**Content Image:** The image you want to transfer the style onto. 

**Style Image:** The image you want to transfer the style from. 

**Generated Image:** The output image, which starts as a copy of the content image and is iteratively refined. 


## Implementation Details
### Feature Extraction:

Used the VGG-19 model (without the top classification layers) to extract features from selected layers.
Selected intermediate layers for content and early to deep layers for style.

### Loss Functions:

**Content Loss:** Measures the difference in content between the generated and content images.
**Style Loss:** Measures the difference in style between the generated and style images. It uses the Gram matrix to capture style information.
**Total Loss:** A weighted combination of content and style loss.

### Optimization:

Initialized the generated image as a copy of the content image.
Used the Adam optimizer to minimize the total loss and update the generated image.

### Visualization:
Visualized the content, style, and generated images at various stages of the optimization process.
