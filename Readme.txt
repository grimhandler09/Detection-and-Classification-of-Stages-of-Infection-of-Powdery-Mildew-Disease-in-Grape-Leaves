The Following Files contain a pipeline to Detect and Classify the Stages of Infection of Powdery Mildew Disease in Grape Leaves.
The Pipeline consists of 4 Parts
1. A U-Net model to perform Semantic Segmentation to detect the foreground and create a mask making it our RoI
2. A cropping algorithm takes the mask produced from the U-Net, crops the RoI from the background, and saves it.
3. Classification using a simple Convolutional Neural Network to determine the stages of Infection [0: Least Infected.... 5: Highly Infected]
4. A final Integration that takes all 3 codes and creates a pipeline.