# weed-detection-in-corn-field
If you require automatic weed detection in a cornfield, this tool is a valuable resource. It operates on a trained Random Forest model using a dataset consisting of over 20,000 polygons representing corn and weeds. 

![image](https://github.com/AliBgisrs/weed-detection-in-corn-field/assets/109620013/f8236615-08b0-450e-9bd2-35c01fb81d45)


Table of Contents

•	Installation
•	Usage
•	Contributing
•	License

Installation

ARCGIS PRO version 3

[Download the tool and the "rfw1.pkl" model]

[Go to the insert tab of your ArcGIS PRO project]

![image](https://github.com/AliBgisrs/weed-detection-in-corn-field/assets/109620013/53edd938-5258-41e3-a29b-6566a277bc11)
 
[Select add folder and browse to the folder that you have saved your script and add that folder]

[Go to the Catalog and find your folder in the Folders section and then find the tool with the name of weed_detection_RF_Ali.atbx, then open it to find the script]
  
 ![image](https://github.com/AliBgisrs/weed-detection-in-corn-field/assets/109620013/7a241b49-cef4-4e17-9826-11e0d695fa65)
 
![image](https://github.com/AliBgisrs/weed-detection-in-corn-field/assets/109620013/14998a20-3882-4e88-b4af-1608caf26ab6)

 [Double click and open the script]

 ![image](https://github.com/AliBgisrs/weed-detection-in-corn-field/assets/109620013/5dc7d027-9af7-4510-9641-5d52072edf6d)


Specify the input file (NDVI). The output directory should be the folder where you intend to save the results. The model directory should be the folder where “rfw1.pkl” model is located.

Usage

If you need automated weed detection in a cornfield, this tool is an invaluable asset. It utilizes a pre-trained Random Forest model, trained on a dataset containing more than 20,000 polygons representing both corn and weeds. The tool's workflow begins by segmenting the NDVI image into smaller parts based on a defined cut-off value. Subsequently, it computes several shape metrics for each segment, including area, perimeter, shape index, compactness, length, and width. These calculated shape metrics are then used as input features for the trained Random Forest model, facilitating the classification of corn and weeds.

 ![image](https://github.com/AliBgisrs/weed-detection-in-corn-field/assets/109620013/88f7665e-5c00-4cac-96fc-b90648446c98)

NDVI image that shows the rows of corn and weeds.
 ![image](https://github.com/AliBgisrs/weed-detection-in-corn-field/assets/109620013/2eac6b12-3ba7-4e1f-b03e-60a3031c4c94)


 
Upon running the tool, you will discover a geodatabase named "66.gdb" in the specified output directory. Within this geodatabase, you'll find the extracted results thoughtfully organized and stored for your convenience.  
![image](https://github.com/AliBgisrs/weed-detection-in-corn-field/assets/109620013/b6d57aad-76af-43af-8328-516c9e9c7cab)

![image](https://github.com/AliBgisrs/weed-detection-in-corn-field/assets/109620013/9cfd65eb-56c6-48db-9732-d5a83b776af5)
 
Output_polygon_features: the initial polygon of segmented NDVI
Shape metrics layer: the results of shape metrics for each polygon
finalPrediction: a database that contains the prediction column

 ![image](https://github.com/AliBgisrs/weed-detection-in-corn-field/assets/109620013/002b003b-eea7-4572-9858-fac307f42c72)

finalPrediction table


Open the "Output_polygon_features" and "finalPrediction" layers in ArcMap and utilize the "Join Field" operation to combine their tables. This will enable you to observe the prediction results for each polygon. You can further enhance the visualization by creating a symbology or save the results to a new directory for future reference. The "Join Field" operation should be performed based on the "ObjectID" field in the "Output_polygon_features" layer and the "ID" field in the "finalPrediction" table. This will ensure a proper and accurate joining of the tables.
![image](https://github.com/AliBgisrs/weed-detection-in-corn-field/assets/109620013/750bfa24-662a-4943-847a-41578b0f3d33)

 
Please be mindful that when running the tool again, it's important to either use a new directory or delete the existing "finalPrediction" file prior to execution. This will help prevent any conflicts or issues during the process.
In the "Prediction" field, a value of 1 represents corn, and a value of 0 indicates weed.
 
![image](https://github.com/AliBgisrs/weed-detection-in-corn-field/assets/109620013/c373a5ec-4975-4b29-b6fe-ac65ef04d104)



Contributing

Please execute the script, utilize its functionalities, and provide me with your valuable suggestions to enhance its performance.


License

About the Author

[Developed by Aliasghar Bazrafkan.]

Acknowledgments

[I would like to express my sincere appreciation to my supervisor, Dr. Paulo Flores, from North Dakota State University (NDSU), for providing invaluable support and guidance throughout the development of this script. His expertise and encouragement have been instrumental in making this project possible].

Contact

[Aliasghar.bazrafkan@ndus.edu]

Additional Notes

[https://sites.google.com/ndsu.edu/floreslab/home?authuser=0]
