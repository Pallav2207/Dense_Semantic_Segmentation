# Hurricane Harvey || Deep Learning  Challenge : Semantic Image Segmentation of Aerial Imagery
##Abstract:
The assignment aimed at implementing deep learning techniques to segment images acquired by a small UAV after Hurricane Harvey in Houston, Texas. The objective was to segment 27 categories of images, such as roof, trees, pools, etc. A group of two students was formed to increase the performance of the baseline model by designing and implementing a deep learning model. The model was trained using 299 training images with pixel-wise annotations and evaluated based on the dice score. The best performing model was DeepLabV3 with Resnet-101 backbone, which outperformed the baseline by 6.97 with a score of 75.09.

##Data Description:
The dataset consisted of 299 training images and 75 test images with shapes of approximately 3000 pixels x 4000 pixels x 3 channels for images and 3000 pixels x 4000 pixels x 1 channel for masks. The images were in TIFF format and masks in PNG format.

##Pre-processing:
Pre-processing steps included final image resize, augmentations, and custom patching. Images were resized to different shapes using the inter_nearest method in the cv2 library. Augmentations were performed on the train and validation set images and masks, including horizontal and vertical flipping and varying brightness and contrast. Custom patching involved reducing all images to the closest square shape of 512 pixels x 512 pixels on the horizontal axis.

##Methodology:
The group attempted multiple semantic segmentation architectures, with the best 3 being DeepLabV3, Feature Pyramid Network (FPN), and U-Net. DeepLabV3 consisted of an encoder network based on a pre-trained CNN and a decoder network added on top of the encoder to refine the segmentation results. FPN combined high-resolution features from a shallow layer of a CNN with semantic information from a deeper layer to improve accuracy. U-Net consisted of an encoder-decoder architecture, where the encoder extracted features from the input image and the decoder up-sampled the features to predict the final segmentation results.
