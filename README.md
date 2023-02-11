# Hurricane Harvey || Deep Learning  Challenge : Semantic Image Segmentation of Aerial Imagery
## 1. Abstract:
The assignment aimed at implementing deep learning techniques to segment images acquired by a small UAV after Hurricane Harvey in Houston, Texas. The objective was to segment 27 categories of images, such as roof, trees, pools, etc. A group of two students was formed to increase the performance of the baseline model by designing and implementing a deep learning model. The model was trained using 299 training images with pixel-wise annotations and evaluated based on the dice score. The best performing model was DeepLabV3 with Resnet-101 backbone, which outperformed the baseline by 6.97 with a score of 75.09.

## 2. Data Description:
The dataset consisted of 299 training images and 75 test images with shapes of approximately 3000 pixels x 4000 pixels x 3 channels for images and 3000 pixels x 4000 pixels x 1 channel for masks. The images were in TIFF format and masks in PNG format.

## 3. Pre-processing:
Pre-processing steps included final image resize, augmentations, and custom patching. Images were resized to different shapes using the inter_nearest method in the cv2 library. Augmentations were performed on the train and validation set images and masks, including horizontal and vertical flipping and varying brightness and contrast. Custom patching involved reducing all images to the closest square shape of 512 pixels x 512 pixels on the horizontal axis.

## 4. Methodology:
The group attempted multiple semantic segmentation architectures, with the best 3 being DeepLabV3, Feature Pyramid Network (FPN), and U-Net. 

Deeplabv3: Deeplabv3 is a state-of-the-art deep learning architecture for semantic segmentation. It uses an Atrous Spatial Pyramid Pooling (ASPP) module to capture contextual information from the input image and produce dense per-pixel predictions. The architecture is a fully convolutional network that utilizes the residual connections for learning fine-grained features. DeepLabV3 consisted of an encoder network based on a pre-trained CNN and a decoder network added on top of the encoder to refine the segmentation results. 

FPN: FPN, or Feature Pyramid Network, is an architecture used for object detection and semantic segmentation. It is based on the idea of creating a pyramid of feature maps, where each level represents a different scale of the input image. This allows the network to effectively detect objects of different sizes and shapes in an image. The FPN architecture consists of a backbone network, such as ResNet, and a top-down pathway that generates the feature pyramid.FPN combined high-resolution features from a shallow layer of a CNN with semantic information from a deeper layer to improve accuracy. 

U-Net: U-Net is a convolutional neural network architecture designed for biomedical image segmentation. It consists of an encoder-decoder structure, where the encoder generates a feature map of the input image and the decoder generates the final segmentation map. The architecture is called U-Net because the decoder is symmetrically connected to the encoder, forming the shape of a "U". The U-Net architecture is useful for semantic segmentation tasks because it effectively combines local and contextual information from the input image. U-Net consisted of an encoder-decoder architecture, where the encoder extracted features from the input image and the decoder up-sampled the features to predict the final segmentation results.

## 5. CONCLUSION
In conclusion, this project aimed to solve a remote sensing problem using deep learning techniques. The task was to perform the dense segmentation of aerial images acquired by a small UAV in the aftermath of Hurricane Harvey. The project team attempted several different semantic segmentation architectures, including DeepLab V3, Feature Pyramid Network, and U-Net.

The best performing model was DeepLab V3 with ResNet-101 backbone, achieving a maximum mean dice score of 75.09, which outperformed the baseline by 6.97. The project team found that the combination of the encoder-decoder architecture and the Atrous convolutions in DeepLab V3 allowed the model to capture context at multiple scales and refine the segmentation results.

Overall, this project demonstrated the potential of deep learning techniques in solving remote sensing problems, and showed the importance of careful design and implementation of deep learning models in order to achieve high performance.




