## **README - Assignment No. 4**



**Course:** Machine Learning



**Assignment:** Convolutional Neural Networks (CNNs) - Flowers102 Classification



**Authors:**

Topaz Aakal, 318644549

Tom Hilton, 318780343



###### **1. GitHub Repository**

This project is hosted on GitHub



**GitHub link:**

https://github.com/tomhil/Assignment4.git



###### **2. Repository Contents**

The repository includes:

* sample.ipynb
  Contains:
  -VGG implementation (transfer learning for Flowers102)
  -YOLOv5 classification experiment where we manually replace the classifier head (1000 -> 102)
* yolo.ipynb
  Contains:
  The best-performing YOLOv5 transfer learning workflow, using YOLOv5’s native classification training scripts (the recommended Ultralytics approach)



###### **3. Description of the Solution**

The goal of this assignment is to perform fine-grained image classification on the Flowers102 dataset (102 flower categories) using CNN-based models and transfer learning. We trained and evaluated two main approaches:



1. **VGG Transfer Learning (baseline CNN classifier)**

-Uses an ImageNet-pretrained VGG model

-Replaces the final classifier layer to output 102 classes

-Trains and evaluates the model on stratified splits



**2. YOLOv5-CLS Transfer Learning (classification backbone)**
Two variants:

\-Manual head replacement (in sample.ipynb) 
Load yolov5s-cls.pt, replace the last linear layer to output 102 classes, optionally freeze the backbone and train using our own training loop.



**-**Native YOLOv5 classification training (in yolo.ipynb)
Uses the official YOLOv5 classification scripts (classify/train.py, classify/val.py) for training and evaluation, producing the strongest results.


All experiments report accuracy and cross-entropy loss as a function of epoch, as required.


###### **4. How to Run the Notebook**

1. Clone the repository

*git clone https://github.com/tomhil/Assignment4
cd Assignment4*


3. Run the notebooks

*jupyter notebook*


Open and run one of:

sample.ipynb 

yolo.ipynb 


###### **5. Output and Results**

Running the notebooks produces:

* Accuracy curves (Train/Validation/Test)
* Cross-Entropy loss curves (Train/Validation/Test)
* Final evaluation results on test split
* For yolo.ipynb: YOLO training run folders (including results.csv and saved weights such as best.pt)





