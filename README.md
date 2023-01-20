# Introduction:
An important step in various agriculture-related remotely sensed pipelines is the precise segmentation of huge amounts of land. The boundaries help to identify the different pastures of land adjacent to each other which may or may not have similar or dissimilar crop types. the Deep Learning approach was considered for the required task of field delineation. Various convolutional networks were used for image segmentation due to their proven reliability in image processing. The focus was to figure out an effective and viable way for identifying the boundaries of the fields and segmenting the croplands accurately.

# Key Differentiators of my work: 
1.	Figured out a way to quickly access satellite imagery data of farmlands.
2.	Processed the image on 4 bands compared to conventional 3 bands.
3.	Normalized the image using NDVI for effective detection of boundaries.
4.	Hyper tuned the parameters of Satellite UNet which is designed for handling satellite images.
5.	Chose the optimum hyper parameters for Adam Optimizer for this task.
6.	Achieved 95% accuracy, 5 percent increase as compared to previous methods.
7.	Figured out a way to export the image into GeoTIFF format and converted them into vector polygon files to incorporate into ArcGIS software.

# Folder Structure:

Notebooks: Contains all the code. Divided into Traning, Testing and Prediction notebooks

Data: Contains original and ground truth data for sample area and the link to entire data

Networks: Contains all the trained model files

Prediction on Seen Data: Contains the prediction on Data from Training run itself

Prediction on Unseen Data: Contains the prediction on Data from unseen data i.e Nagpur

# Project Flow:
 1.	Choosing Data and Study Area:
The study area is chosen the Netherlands. I chose Netherlands due to the availability of ground truth data for Netherlands fields. In the figure below, the distribution of fields is shown on the map of the Netherlands:
 ![image](https://user-images.githubusercontent.com/87564754/213633900-fc4db49f-29b4-483a-a28e-9f465ebca837.png)


2.	Data Preprocessing:
a.	Converting Images into Pixel-Wise Arrays
b.	Normalizing the image
c.	Setting up training and testing data set

3.	Model Development:
a.	UNet Model Development
b.	FCN Model Development
c.	Choosing the Hyperparameters for the same

4.	Model Training

5.	Model Testing

6.	Making Predictions

7.	Postprocessing: Converting the GeoTiff files into polygon files
![image](https://user-images.githubusercontent.com/87564754/213633866-adf41d47-0e0a-41bb-bd36-03b2db04fb9b.png)


# Deployment:
I deployed the project using a template provided by StreamLit. Where I incorporated the field boundaries for nagpur with the point data of crops and joined the polygons and crop data through a common ID. The map was used from mapbox. The result was as follows:
![image](https://user-images.githubusercontent.com/87564754/213633025-8920f209-b0f1-4744-a918-cfdd55e121c1.png)
 
The crops are represented through different colors and the gray fields represent unavailable crop data.
If hovered over a single crop, it displays the crop data for the same.
![image](https://user-images.githubusercontent.com/87564754/213633779-4af3c8c3-d845-43b8-8911-f7108483baf9.png)
