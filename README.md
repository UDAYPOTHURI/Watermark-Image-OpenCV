# Watermark-Image-OpenCV

This project uses OpenCV to add a watermark to an image. The watermark is added as text and can be rotated and resized.

## Installation

To use this project, you'll need to have OpenCV, Urllib3 and NumPy installed. You can install them using pip:

pip install opencv-python

pip install urllib3

pip install numpy

You'll also need to download the `Watermark-Image-OpenCV.ipynb` file from the GitHub repository. You can do this by clicking on the "Code" button on the repository page and selecting "Download ZIP". Once you've downloaded and unzipped the file, you can open it in a Jupyter notebook.

## Usage

To use this project, simply run the `Watermark-Image-OpenCV.ipynb` file in a Jupyter notebook. You'll be prompted to enter the watermark text. The code will then add the watermark to an image and display the result.

Here's a detailed explanation of how the code works:

1. The code starts by importing the necessary libraries: `cv2`, `urllib`, and `numpy`.
2. It then reads an image from a URL using `urllib.request.urlopen()` and converts it into a NumPy array using `np.asarray()`.
3. The image is then decoded using `cv2.imdecode()` and displayed using `cv2.imshow()`.
4. The image is resized to 300x300 pixels using `cv2.resize()`.
5. A black image is created using `np.zeros()`.
6. The shape of the black image is obtained using `.shape`.
7. The user is prompted to enter the watermark text using `input()`.
8. The watermark text is added to the black image using `cv2.putText()`.
9. A rotation matrix is created using `cv2.getRotationMatrix2D()`.
10. The black image is rotated using `cv2.warpAffine()`.
11. The black image is resized to match the size of the original image using `cv2.resize()`.
12. The original image and the black image are combined using `cv2.addWeighted()`.
13. The watermarked image is saved to disk using `cv2.imwrite()`.

![output image](image.png)