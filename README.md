
## WHAT IS A CNN AUTOENCODER ?
 Input Image
      │
      ▼
  Encoder
(Compresses image)
      │
Compressed Features
      │
      ▼
  Decoder
(Reconstructs image)
      │
      ▼
Output Image (Denoised)

# IMAGE DENOISING USING CONVOLUTIONAL AUTOENCODER
MY IMPLENTATION USES A CONVOLUTIONAL AUTOENCODER INSTEAD OF A DENSE AUTOENCODER BECAUSE CONVOULTIONAL LAYERS ARE BETTER SUITED FOR IMAGE DENOISING TASKS BY PRESERVING LOCAL SPATIAL FEATURES.

The model is trained using the MNIST dataset and learns to reconstruct clean images from noisy input .

## OBJECTIVES

- Load and preprocess the MNIST image dataset.
- Added Gaussian noise to simulate corrupted images.
- Build a Convolutional Autoencoder using TensorFlow/Keras.
- Train the model to reconstruct clean images.
- Compare the original, noisy, and denoised images.
- Evaluated reconstruction quality using Mean Squared Error (MSE).

##  Dataset

**Dataset:** MNIST Handwritten Digits

- Training Images: 60,000
- Testing Images: 10,000
- Image Size: 28 × 28 pixels
- Color Mode: Grayscale

Dataset Structure:

```
dataset/
└── mnist_png/
    ├── training/
    │   ├── 0
    │   ├── 1
    │   ├── ...
    │   └── 9
    └── testing/
        ├── 0
        ├── 1
        ├── ...
        └──9

        
## TOOLS USED    
1- PYTHON 
2- TENSORFLOW / KERAS
3- NUMPY
4- MATPLOTLIB
5- SCIKIT-LEARN

### Encoder
- Conv2D (32 filters, 3×3, ReLU)
- MaxPooling2D
- Conv2D (64 filters, 3×3, ReLU)
- MaxPooling2D

### Decoder
- Conv2D (64 filters, 3×3, ReLU)
- UpSampling2D
- Conv2D (32 filters, 3×3, ReLU)
- UpSampling2D
- Conv2D (1 filter, Sigmoid)

## STEPS WE USED 

Load the mnist dataset
normalize pixel values
Add gausian noise to images
Build the CNN Autoencoder
Train the MOdel
predicted the denoised images
compare orignal , noisy and recontructed images
evaluate model performance using MEAN SQUARED ERROR.

AT THE END
## RESULT
The trained autoencoder successfully reconstructs cleaner handwritten digit images from noisy inputs.

The project includes:
- Sample original images
- Noisy images
- Denoised output images
- Training and validation loss curves
- Mean Squared Error (MSE) evaluation

  --Future Improvements

- Train for more epochs to improve reconstruction quality.
- Experiment with deeper autoencoder architectures.
- Use Batch Normalization and Dropout.
- Test the model on real-world noisy image datasets.
- Compare performance with Denoising CNN (DnCNN) and U-Net.

## Author

** Khushi Yadav**