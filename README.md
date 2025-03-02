# Coin Segmentation and Counting

## **Project Overview**
This project performs **coin segmentation and counting** using **OpenCV and Python**. The process includes:
- Detecting **edges and contours** in an image.
- Applying **region-based segmentation** to isolate individual coins.
- Converting the image to **HSV color space** for better segmentation.
- Applying **gray color masking** to focus on coin regions.
- Using **Hough Circle Transform** to detect and count circular objects.
- Displaying **segmented coins** and labeling them with their count.

## **How to Run the Code**
### **1. Install Required Dependencies**
Before running the Jupyter Notebook, install the required libraries using:
```bash
pip install opencv-python numpy matplotlib
```

### **2. Open the Jupyter Notebook**
Start Jupyter Notebook using:
```bash
jupyter notebook
```
Then open the notebook file (`coin_segmentation.ipynb`).

### **3. Run the Notebook Cells**
- Load the image.
- Preprocess the image (convert to **HSV**, grayscale, thresholding, morphological operations, edge detection).
- Detect and segment the coins.
- Show the results, including detected coins and individual coin images.

## **Methods Used**
### **1. Preprocessing**
- Convert the image to **HSV color space** to handle lighting variations.
- Extract the **Value (V) channel** to enhance contrast.
- Apply **gray color masking** to isolate potential coin regions.
- Apply **Gaussian Blur** to remove noise.
- Use **adaptive thresholding** and **morphological operations** to refine edges.
- Apply **Canny edge detection** to highlight coin boundaries.

### **2. Contour Detection and Filtering**
- Detect contours using `cv2.findContours()`.
- Filter contours based on **area and hierarchy** to remove noise.

### **3. Hough Circle Transform for Coin Detection**
- Apply `cv2.HoughCircles()` to detect circular objects (coins).
- Label detected coins with numbers using `cv2.putText()`.

### **4. Extracting and Displaying Individual Coins**
- Use `cv2.boundingRect()` to extract each coin.
- Display each extracted coin separately using `cv2.imshow()` or Matplotlib.

## **Results and Observations**
- The algorithm **successfully detects and counts** coins in various images.
- **HSV conversion** improves detection in images with **lighting variations**.
- **Gray color masking** helps in filtering out non-coin regions.
- **Hough Circle Transform** improves accuracy in detecting circular objects.
- **Canny edge detection** enhances contour definition for better segmentation.
- Some **false detections** may occur if background noise is not removed properly.
- False detection can also occur if coins are **shiny**, as reflections may interfere with edge detection.
- Adjusting **morphological operations and Hough Transform parameters** can improve accuracy.

## **Dependencies**
To run this project, you need:
- Python 3.x
- Jupyter Notebook
- OpenCV (`cv2`)
- NumPy
- Matplotlib

## **Future Improvements**
- Improve **adaptive thresholding** for better segmentation.
- Implement **machine learning-based object detection** for more accuracy.
- Enhance visualization with **bounding circles instead of rectangles**.

---
This README provides all necessary details to run and understand the project. Happy coding! 🚀

