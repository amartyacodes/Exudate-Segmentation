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
![exudates](https://user-images.githubusercontent.com/44440114/114542199-4785f480-9c75-11eb-803d-8523c6cb7338.png)
### Now we will know where are the exudates by comparing the images
![final](https://user-images.githubusercontent.com/44440114/114542361-7308df00-9c75-11eb-9e2a-82843e21c264.png)
# Credits
## Papers taken for reference 
1.Guimarães, Juliana & Amorim, Luciana & Ferreira, Flávia & Peixoto, Zélia. (2019). Automatic segmentation of blood vessels in retinal images using 2D Gabor wavelet and sub-image thresholding resulting from image partition. Biomedical Engineering. 39. 10.1007/s42600-019-00028-9. 


2. A. Elbalaoui, M. Boutaounte, H. Faouzi, M. Fakir and A. Merbouha, "Segmentation and detection of diabetic retinopathy exudates," 2014 International Conference on Multimedia Computing and Systems (ICMCS), Marrakech, Morocco, 2014, pp. 171-178, doi: 10.1109/ICMCS.2014.6911368.

