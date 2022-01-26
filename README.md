# Analysis-of-Reforestation-Potential-in-Pakistan

While forests play an important role in mitigating the effects of climate change, the process of reforestation is expensive, difficult to plan and hard to execute and maintain. Therefore, it is important to understand the efficiency of reforestation efforts and develop solid estimates of areas where such efforts will actually yield results.
Using satellite imagery, terrain, and weather data as an input to a machine learning algorithm, this system aims to determine the potential vs actual vegetation cover. Once sufficient data is fed into the algorithm, it’s expected to automatically identify geographical regions with high potential for future reforestation or afforestation efforts.

PROJECT DEVELOPMENT METHODLOGY 

The development methodology of this research shall be divided into two parts namely, Annotations and Classification. 
Annotations:  
a)	Generate multiple sequential satellite images by dividing the total image into smaller parts. 
b)	Assign the indices, NDVI, NDWI, CI, UI etc. Using these indices, for every polygon image that has been filtered out, we can randomly select some points from every image to get the average indices for that area. That will help us in mapping those areas with these indices. Based on these indices, we can then assign a label to the area in terms of a Forest, farm, urban etc. 
The following formulae shall be used to calculate the indices: 
NDVI = (NIR - RED) / (NIR + RED)
NDWI = (NIR – SWIR) / (NIR + SWIR)
NDBI = (SWIR – NIR) / (SWIR + NIR)
EVI = G * ((NIR - RED) / (NIR + C1 * RED - C2 * BLUE + L))
Here G = 2.5, L = 1, C1 = 6, C2 = 7.5.
UI = (SWIR2 - NIR)/(SWIR2 + NIR)
Clay Minerals Ratio = SWIR1 / SWIR2
Ferrous Minerals Ratio = SWIR / NIR

Classifications:
The classification of the dataset is done using K-means clustering for now.

