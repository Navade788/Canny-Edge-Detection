# CANNY EDGE DETECTION

## Aim
To implement the Canny Edge Detection algorithm using Python and OpenCV to detect edges in a sample image.

---

## Software Required
1. Anaconda – Python 3.7  
2. OpenCV  
3. Matplotlib  

---

## Algorithm

### Step 1:
Import the required libraries such as OpenCV and Matplotlib.

### Step 2:
Read the input image and convert it into grayscale.

### Step 3:
Apply the Canny edge detection algorithm using `cv2.Canny()`.

### Step 4:
Display the grayscale image and detected edge image using Matplotlib.

### Step 5:
Analyze the effect of different threshold values on edge detection.

---

## Program

```python
import cv2
import matplotlib.pyplot as plt

# Read image
image = cv2.imread("sample.jpg")

# Convert to grayscale
gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Apply Canny Edge Detection
edges = cv2.Canny(gray, 100, 200)

# Display images
plt.figure(figsize=(10,5))

plt.subplot(1,2,1)
plt.imshow(gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")

plt.subplot(1,2,2)
plt.imshow(edges, cmap='gray')
plt.title("Canny Edge Detection")
plt.axis("off")

plt.show()
```

---

## Discussion of Detected Edges

The Canny edge detector successfully identified the boundaries and edges present in the image. Strong edges are clearly highlighted while unwanted noise is reduced.

---

## Impact of Different Parameters

Lower threshold values detect more edges, including unwanted noise.  
Higher threshold values detect only strong and important edges.  
Changing the threshold values affects the thickness, sharpness, and clarity of the detected edges.

---

## Output

<img width="802" height="290" alt="image" src="https://github.com/user-attachments/assets/90218b51-9f8e-42e9-87aa-7690d05854ca" />

---

## Result

Thus, the Canny edge detection algorithm was successfully implemented using Python and OpenCV, and the edges were detected from the sample image.
