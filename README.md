# Image Colorization with GANs

This repository contains a deep learning project that performs image colorization using Generative Adversarial Networks (GANs). The model is designed to take grayscale images as input and generate their colorized versions. A combination of pretraining, U-Net encoder-decoder architecture, and GAN-based fine-tuning ensures high-quality results.

## Features

- **Pretrained Generator**: Utilizes a pretrained generator to kickstart the colorization process.
- **U-Net Architecture**: Employs a U-Net encoder-decoder structure for efficient feature extraction and reconstruction.
- **GAN Training**: Fine-tunes the generator using an adversarial discriminator to enhance realism.

## Model Architecture

### Generator

The generator uses a U-Net encoder-decoder structure:

- **Encoder**: Extracts features from the grayscale input.
- **Decoder**: Reconstructs the colorized image using extracted features.
- **Skip Connections**: Helps retain spatial information from the input image.

### Discriminator

The discriminator is a convolutional neural network that evaluates the realism of the colorized images. It ensures that the generator produces visually plausible results.

### Training Process

1. **Pretraining**: The generator is pretrained using supervised learning with pixel-wise loss (e.g., Mean Squared Error or L1 loss).
2. **GAN Fine-Tuning**: The generator and discriminator are trained together in an adversarial setup:
   - The generator tries to produce realistic colorized images.
   - The discriminator distinguishes real color images from generated ones.

## Dataset

This project is designed to work with grayscale images as input. The output is the corresponding colorized version of the images. For training, the **MiniImageNet** dataset was used, which consists of paired grayscale and color images.
## Requirements

tensorflow==2.10.1
pandas==2.2.3
keras==2.10.0
numpy==1.26.4
matplotlib==3.9.2
joblib==1.4.2

Install dependencies using:

```bash
pip install -r requirements.txt
```
## Training the model
The training process got me some difficulties , I was not able to run the code for so long due to computational issues.
If availible , running the model for long enough by changing the number of epochs and steps can provide better results(highly recommended).
## Models and Weights

- **Model**: [Download Here](https://drive.google.com/file/d/1xxEXxGjkTF1k_Ixhds71QGMSj7zA38yi/view?usp=drive_link)
- **Weights**: [Download Here](https://drive.google.com/file/d/18axZcdYtX_mBAxs2vsMaQcNUxA36wNeH/view?usp=drive_link)

## Acknowledgments

- The project leverages a pretrained generator and builds upon U-Net and GAN architectures.
- Inspired by state-of-the-art image colorization research.

## License

This project is licensed under the MIT License. See `LICENSE` for more details.

---
