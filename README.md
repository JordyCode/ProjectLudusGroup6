# ProjectLudusGroup6

## Dataset division of tasks:

Jordy:
- Made pictures of myself (person) and the paddle
- Configured the Roboflow environement 
- Uploaded all images and grouped them per group member so they could annotate the pictures
- Annotated the pictures that were assigned to me
- Trained the dataset together with the group members

Abhishek:
- Made pictures of myself (person) and the paddle
- Annotated the pictures that were assigned to me
- Trained the dataset together with the group members

Nick:
- Made pictures of myself (person) and the paddle
- Annotated the pictures that were assigned to me
- Trained the dataset together with the group members


## Description of initial choices and preliminary results:
First we tried to train our model with Tensorflow. Here we encountered the problem that humans weren't being detected very well. We started doing some research on different machine learning platforms and had some conversations with other Ludus groups. We decided to switch to Yolov5 together with Roboflow to annotate our dataset instead. This gave us way better results. We've used Python as our programming language. The algorithm we used is Yolo. You can say that all objects are detected via a single algorithm run. It’s done by dividing an image into a grid and predicting bounding boxes and class probabilities for each cell in a grid. Yolo's raw output contains many bounding boxes for the same object, but with a lot of poorly performed boxes. To select the best bounding box for a given object, a non-maximum suppression (NMS) algorithm is applied. 
All boxes that Yolo predicts have a confidence level associated with them. NMS uses these confidence values to remove the boxes which were predicted with low certainty. Usually, these are all boxes that are predicted with confidence below 0.5. We trained our model with a batch size of 32 and 100 epochs. The average accuracy is 0.864. The average loss is based on the three graphs that are in the `yolov5\runs\train\exp\results.png` about train/box_loss (0.01), train/obj_loss (0.004) and train/cls_loss (0.001). We added up those values and divided this which resulted in 0.005 as our average loss.
 
 
 ## Model division of tasks:
 
 Jordy:
- Trained the dataset together with the group members
- Analyse the results together
- Testing the model on webcam and pictures together on school and Discord

Abhishek:
- Trained the dataset together with the group members
- Analyse the results together
- Testing the model on webcam and pictures together on school and Discord

Nick:
- Trained the dataset together with the group members
- Analyse the results together
- Testing the model on webcam and pictures together on school and Discord
