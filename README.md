
# Automated Image Quality Inspection with Amazon Lookout for Vision

## Introduction

In the context of modern technological advancements, this guided project is an exploration into the development of an automated image quality inspection system using Amazon Lookout for Vision. Amazon Lookout for Vision, a prominent Machine Learning as a Service (MLaaS) offered by Amazon Web Services, serves as the cornerstone for this endeavor. It presents an opportunity to delve into the realm of image analytics, enabling the seamless execution of complex tasks without the necessity of writing code.

Amazon Lookout for Vision's versatile capabilities extend to addressing intriguing use cases, including but not limited to drone detection, defect identification, object recognition, smile detection, and fall detection. This project underscores the practical application of Lookout for Vision, demonstrating its prowess in automating intricate image analysis workflows.

The unique aspect of this venture lies in its code-free approach, allowing practitioners to harness the potential of machine learning without delving into the intricacies of programming. As we progress through the project, the focus will be on understanding Lookout for Vision's functionalities and applying them to real-world scenarios, particularly in the context of image quality inspection. This guided exploration aims to empower individuals to leverage Lookout for Vision effectively, showcasing its capacity to revolutionize image analytics effortlessly.

## Dataset Used


The dataset employed in this project was sourced from the Amazon Lookout for Vision GitHub repository, specifically accessible through the following path: https://github.com/aws-samples/amazon-lookout-for-vision/tree/main/circuitboard

This dataset is meticulously designed for circuit board image analysis and is instrumental in achieving the project's primary goal: distinguishing images into anomalies or normal instances.

### Dataset Structure:

The dataset is organized into three main folders:

Train: This folder comprises subfolders for both normal and anomaly classes. The 'normal' subfolder contains images of circuits that are free from defects, representing the standard or normal class. On the other hand, the 'anomaly' subfolder includes images of circuits with various defects.

Test: Similar to the 'Train' folder, the 'Test' folder encompasses subfolders for normal and anomaly classes. It serves as the dataset against which the model's performance is evaluated.

Extra_Images: This folder is pivotal for the trial detection phase. It includes additional images that were not part of the original training or testing sets. These images are used to assess the model's performance on previously unseen data.

#### Subfolder Details:

#### Normal Subfolders: 
Images in these subfolders represent circuit boards without any defects, providing the baseline for the 'normal' class in the classification task.

#### Anomaly Subfolders: 
Images in these subfolders depict circuit boards with various defects, serving as instances of the 'anomaly' class.

This dataset structure ensures a comprehensive representation of both normal and anomalous instances, facilitating the training and evaluation of the image classification model using Amazon Lookout for Vision.

## Steps Used

The project aimed to automate image quality inspection using Amazon Lookout for Vision, a Machine Learning as a Service (MLaaS) from AWS. The dataset, downloaded from the provided path, included normal and anomaly images of circuit boards. The workflow encompassed creating a project workspace, exploring, uploading, and labeling the dataset. A classifier model was trained to predict circuit board defects. Performance metrics were evaluated, followed by trial detection on new images. Feedback from trial detection informed the retraining of the model for potential accuracy improvement.

Steps:
Learn about AWS Lookout for Vision Service

Create a Project Workspace

Explore, Upload, Label Dataset

Train Model

Evaluate Performance Metrics

Run Trial Detection

Retrain the Model

## Create Project

Click on "get started":

insert image 1

Benefits & Features:

image 2

Use Cases:

image 3

Click on "create project:

Name the project as lookout-vision and click on create project.

image 4




## Explore, Upload, & Label Dataset

Click on "create dataset":

image 5


Given that our dataset is already partitioned into distinct training and testing subsets, we will proceed with the second configuration option:

image 6

We'll be uploading images directly from our local computer:

image 7

Similarly, we will upload images from our local computer for the test dataset:

image 8


Afterwards, we proceed by selecting "Create Dataset." The subsequent step involves the upload of both training and test images:

image 9


Initially, we upload the anomaly images from the training dataset, categorizing them as anomalies, and subsequently repeat this process for the normal images. This sequence is then replicated for the test dataset.

image 10

image 11


## Train Model

Select the "Train Model" option located at the top right corner:

image 12

Once more, proceed by clicking on the "Train Model" option:

image 13

Confirm your selections and proceed by clicking on "Train Your Model":

image 14


The completion of this process is expected to take approximately thirty minutes, with the duration contingent on the volume of data being processed.

image 15

The precision stands at 73.1%, accompanied by a recall rate of 95%.

image 16
## Evaluate the Performance Metrics


In the evaluation, the model was tested on a set of 40 images, resulting in a precision of 73.1%. This means that out of a total of 26 predictions, 19 anomalies were correctly identified. The recall rate of 95% indicates that 19 anomalies were detected out of a total of 20 anomalies present. Consequently, the overall performance of the model is assessed at 82.6%.

image 17

image 18

image 19


## Run Trial Detection

A trial detection is initiated to assess the model's performance in identifying anomalies within a set of new images:

image 20

image 21

Choose the option to upload images from your computer, then proceed to select "Detect Anomalies." Finally, opt for "Run Trial Detection."

image 22

Next, upload the images for analysis:

image 23

Upload all the images from the "extra_images" dataset. The process is expected to run for approximately 20 minutes. Upon completion of the trial detection, the model has predicted 9 instances as normal and identified 11 instances as anomalies:

image 24

Additionally, there are 20 images that are yet to be verified. We will manually assign labels to these images:

image 25

Then click on "Then add verified to training dataset".


## Retrain the Model

For the retraining of the model, navigate to the dataset section. Observe that this time, the training dataset comprises 60 images due to the addition of 20 images. Proceed by clicking on "Train Model." The current configuration includes 60 training and 40 test images.


image 26

Then click on "train model":

image 27

The training process for this model is anticipated to require approximately 40-45 minutes.

The model has completed training, achieving an accuracy of 95% and a precision of 86.4%:

image 28

Select "Model 2" to review the performance metrics:

image 29

The precision has now shown improvement compared to the previous iteration, advancing from 73.1% to 86.4%. This enhancement is attributed to the labeling of images and the subsequent feedback loop, wherein the labeled data was reintroduced for the retraining of the model.

image 30


## Conclusion

In conclusion, this project successfully harnessed the capabilities of Amazon Lookout for Vision to automate image quality inspection without the need for manual coding. The dataset, comprising normal and anomaly images of circuit boards, served as the foundation for creating a robust classifier. The initial model, trained on this dataset, exhibited a precision of 73.1% and a recall of 95%. Following model evaluation, a trial detection phase was initiated, leading to valuable feedback. Leveraging this feedback to augment the training dataset, the model underwent retraining, resulting in a substantial improvement. The final iteration of the model achieved an impressive accuracy of 95% and a precision of 86.4%. This iterative process not only validated the effectiveness of the chosen MLaaS but also underscored the project's commitment to continual refinement, emphasizing the practical impact of machine learning in automated image analytics.
