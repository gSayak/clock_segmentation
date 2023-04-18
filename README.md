<h1>Clock Detection using Mask R-CNN</h1>

This project uses Mask R-CNN to detect clocks in images. The model is trained on a custom dataset and can accurately detect clocks in various settings.

<h2>Dataset</h2>
The dataset used for this project consists of 128 images of clocks, along with their respective annotations. The images were sourced from various websites and were manually annotated using MakeSense.ai.

The dataset can be found in the dataset directory of this repository.

It contains the annotations.json file and the images.zip

<h2>Steps to run the code</h2>

1. Load the 'clock-detection.ipynb' in the google collab.
2. Connect the collab to a runtime and change the runtime type to GPU. (runtime -> runtime type ->hardware acclerator -> GPU)
3. Upload the annotations.json and the images.zip to the collab either using drag and drop or by uploading it to your drive and connecting the drive to the notebook.
4. In the notebook, go to the '2. Image Dataset' code and in the cell update the 'images_path' and the 'annotations_path' with the path of the images.zip and the annotations.zip respectively.


   ![](https://github.com/gSayak/clock_detection/blob/main/readme_images/clock_annotations.png)
   ![](https://github.com/gSayak/clock_detection/blob/main/readme_images/clock_annotations2.png)
   ![](https://github.com/gSayak/clock_detection/blob/main/readme_images/clock_annotations3.png)
   ![](https://github.com/gSayak/clock_detection/blob/main/readme_images/clock_annotations4.png)


5. Next keep running the respective cells and then wait for the 5 epochs to run which might take some time.
6. In the '4. Detection' you'll see two images, first one which is the result of the training of our model on the custom-dataset and the next one is the annotated result of the dataset.


![](https://github.com/gSayak/clock_detection/blob/main/readme_images/clock1.png)
![](https://github.com/gSayak/clock_detection/blob/main/readme_images/clock2.png)


7. Running it multiple times, random images will be tested from the dataset.

<h2>Steps to run the code on your own trained model</h2>

1. From the previous steps go to Mask_RCNN -> logs -> object-name and download the mask_rcnn_object_0005.h5.
2. Run till the '2. Run Mask-RCNN on Images'.
3. Drag and drop the '.h5' model and update the path of 'load_inference_model(1, "/path/to/model.h5") and upload an image to test your dataset and update the path of img = cv2.imread("/path/img.jpg")

![](https://github.com/gSayak/clock_detection/blob/main/readme_images/clock_test.jpg) 

4. Run the following cells and you will get the masked picture of your clock.

![](https://github.com/gSayak/clock_detection/blob/main/readme_images/clock_test2.png)
