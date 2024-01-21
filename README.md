# Improved-Crack-Detection-on-Road-Surfaces-with-Image-Processing
This work proposes a generative adversarial network (GAN) type SpA-Former model to generate shadow-free images. Inverse perspective mapping (IMP) is performed through OpenCV libraries, where it computes the coordinates of the converging road lines observed from an angle perspective view and warps them into bird-eye view (BEV) perpendicular to the road surface. The processed images are passed through the EnlightenGAN to enhance the details of low-light images while reducing the noise. Later, transfer-learned ResNetV2, VGG19, DenseNet201, MobileNet-V2 and EfficientBetB7 models with ImageNet weights use the processed images for model training to classify the presence of road cracks.

Compare the effectiveness of the image classification with the influence of:
* shadow removal
* enlightenGAN

The datasets were compared from raw (road_surface_raw), with shadow removal (road_surface_shadow), and with both shadow removal and enlightenGAN (road_surface_processed):

![image](https://github.com/wzhau998/Improved-Crack-Detection-on-Road-Surfaces-with-Image-Processing/assets/137457605/856274da-687d-49fe-9906-a34c02856262)

# How to use
* Download and upload the three rar file datasets to Google Drive
* Open CNN detection.ipynb in Google Colab
* Edit the dataset path of the datasets, then run the Google Colab
* It is recommended to use T4 GPU to run the code
