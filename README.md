# Exudate-Segmentation
Project on Segmentation of Exudates through Image Processing Techniques
## Image Dataset 
https://ieee-dataport.org/open-access/indian-diabetic-retinopathy-image-dataset-idrid
### Sample Image
![download](https://user-images.githubusercontent.com/44440114/114540923-b6624e00-9c73-11eb-8e92-c643274e7e63.png)
### Taking the Green Channel of the image and apply CLAHE (Contrast Limited Adaptive Histogram Equalisation) 
![clahe](https://user-images.githubusercontent.com/44440114/114541219-0c36f600-9c74-11eb-99e0-84a80ce9e75d.png)

### After Taking CLAHE of the green channel image I am using alternate sequential filtering for Blood Vessel Extraction
![bv image](https://user-images.githubusercontent.com/44440114/114541416-54eeaf00-9c74-11eb-942c-472769ace95f.png)
### The edge candidates
For edge candidates , first we find the edges using Canny Edge Detection and then subtracting the blood vessels from he image using the given function 
![edge](https://user-images.githubusercontent.com/44440114/114541822-d47c7e00-9c74-11eb-8392-1ee9111044d0.png)
### Now in order to remove the outer edge , we take a mask just as the same shape of the image and then perform a bitwise AND with the image
