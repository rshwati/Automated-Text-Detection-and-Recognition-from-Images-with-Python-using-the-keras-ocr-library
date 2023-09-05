# Automated-Text-Detection-and-Recognition-from-Images-with-Python-using-the-keras-ocr-library
Automates the process of text detection and recognition on a batch of images, facilitating efficient data extraction from images for various applications, including document digitization and information retrieval


The provided code snippet serves as a key component within a text detection and recognition project. Its primary purpose is to process a batch of images, apply text detection and recognition techniques, and save the annotated images. 

**Code Functionality Summary**:

The code serves the following functions within the project:

1. **Image Processing**
2. **Text Detection and Recognition Pipeline**: It initializes a text detection and recognition pipeline using the **`keras_ocr`** library. This pipeline is responsible for identifying and transcribing text from images.
3. **Input and Output Directories**: The input directory contains a batch of images that require text detection and recognition, while the output directory is designated for saving annotated images.
4. **Image File Retrieval**: Using the **`glob`** function, the code retrieves a list of image file paths within the input directory. It accommodates various image formats, such as JPEG, PNG, WebP, and JPG, enabling flexibility in the image data accepted by the system.
5. **Results Storage**: An empty list (**`results_list`**) is created to store the results of text detection and recognition for each processed image. This list will contain information about the detected text and its bounding box coordinates.
6. **Image Processing Loop**: The core of the code lies within a loop that processes each image in the batch. For each image, the following steps are executed:
    - The image is loaded using the **`plt.imread`** function.
    - The Keras OCR pipeline is applied to the image to detect and recognize text, with results stored in **`results_list`**.
    - A subplot is created for displaying the image with text annotations.
    - Detected text is overlaid on the image using **`keras_ocr.tools.drawAnnotations`**.
    - A title is set for the plot.
    - The annotated image is saved to the output directory with the same filename as the original image.
    - The plot is closed to release resources, ensuring efficient processing of subsequent images.
