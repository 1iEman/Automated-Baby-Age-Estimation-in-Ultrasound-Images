# Automated-Baby-Age-Estimation-in-Ultrasound-Images

This simple project automates the estimation of a baby's gestational age based on ultrasound images. It processes 9 sample images through the following steps: 
1. Image Preprocessing:

        Apply Gaussian blur and Canny edge detection to extract contours.

        Perform morphological operations (dilation and erosion).

        Remove small unwanted objects to isolate key structures.

2. Skeletonization:

        The cleaned binary image is skeletonized to highlight main anatomical structures.

3. Contour Detection:

        Contours are extracted from the skeleton image using OpenCV.

        An ellipse is fitted to the contour points to estimate the Biparietal Diameter (BPD).

4. Measurement:

        The major axis of the fitted ellipse is considered the BPD.

        Pixel-to-millimeter conversion is applied using a fixed scale (1 pixel = 0.38 mm).

    Gestational Age Estimation:

        BPD values are matched against a medically referenced lookup table to determine the corresponding week of gestation.
        Reference: https://www.researchgate.net/figure/Biparietal-Diameter-Growth-Rate-Table_tbl10_14718580 
   
The libraries Used:

    OpenCV – for image processing and contour analysis.

    scikit-image – for morphological operations and skeletonization.

    matplotlib – for image display.

    NumPy – for numerical operations.
