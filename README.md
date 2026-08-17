#  Lane Detection

##  Aim

To implement a basic lane detection pipeline using OpenCV by completing missing code segments at specified locations.

---

## Learning Objective

* Understand each stage of image processing
* Learn how to build a complete computer vision pipeline
* Practice writing code in guided sections

**Important Instruction:**
👉 Write code **ONLY in places marked as `# Your Code Here`**
👉 Do NOT modify any other part of the code

---

##  Software Used

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

---

##  Algorithm & Explanation

---

###  Step 1: Import Libraries

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

---

###  Step 2: Read the Image

```python
# Read the image using OpenCV

###
image = cv2.imread("road.jpg")
###
```

---

###  Step 3: Convert to Grayscale

```python
# Convert to grayscale.

###
gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
###
```

---

###  Step 4: Display Images

```python
plt.figure(figsize=(10,5))

###
plt.subplot(1, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 2, 2)
plt.imshow(gray, cmap="gray")
plt.title("Grayscale Image")
plt.axis("off")

plt.show()

###
```

---

###  Step 5: Thresholding

```python
# Apply thresholding

threshold = 
###
cv2.threshold(gray, 150, 255, cv2.THRESH_BINARY)[1]
###
```

---

###  Step 6: Region of Interest (ROI)

```python
# ROI masking already provided
# (Do not modify)
```

---

### Step 7: Edge Detection (Canny)

```python
# Perform Edge Detection

###
edges = cv2.Canny(gray, 50, 150)
###
```

---

###  Step 8: Gaussian Blur

```python
# Apply Gaussian Blur

###
blurred = cv2.GaussianBlur(gray, (5, 5), 0)
###
```

---

###  Step 9: Hough Transform

```python
# Detect lines using Hough Transform

###
lines = cv2.HoughLinesP(
    edges,
    1,
    np.pi / 180,
    threshold=50,
    minLineLength=50,
    maxLineGap=20
)
###
```

---

### Step 10: Lane Detection Logic

```python
# Already implemented
# (Do not modify)
```

---

##  Expected Output

* Original image
* <img width="211" height="135" alt="image" src="https://github.com/user-attachments/assets/95969852-deeb-441a-ae11-3e4d651e2143" />

* Grayscale image
* <img width="221" height="135" alt="image" src="https://github.com/user-attachments/assets/14ee1dd7-9ee8-4643-be2f-f0348a7d1721" />

* Thresholded image
* <img width="227" height="138" alt="image" src="https://github.com/user-attachments/assets/45e69413-2d25-46e3-9e49-561ffa5cd11c" />

* ROI masked image
* <img width="211" height="137" alt="image" src="https://github.com/user-attachments/assets/d60a573a-6c51-4215-81e4-12c007aaf0ea" />

* Edge detected image
* <img width="218" height="140" alt="image" src="https://github.com/user-attachments/assets/9d9b9bc3-3242-4fde-809a-adcb9733cc12" />

* Smoothed image
* <img width="223" height="142" alt="image" src="https://github.com/user-attachments/assets/04f91665-a42e-47b7-a380-44bab371df6f" />

* Detected lines
* <img width="217" height="146" alt="image" src="https://github.com/user-attachments/assets/e6a2b957-e422-4351-9029-c4c87461cfab" />

* Final lane detection output
* <img width="231" height="150" alt="image" src="https://github.com/user-attachments/assets/948423a6-3cf9-4fda-98d3-879511b407b3" />

---

##  Instructions

* Fill ONLY in `# Your Code Here` sections
* Do NOT change existing code
* Run step-by-step
* Verify outputs

---

## Result

Thus, the lane detection pipeline is successfully implemented by completing the missing code sections. The system detects and highlights lane lines effectively.

---

##  Developed By

* **Name:**Cholimgpuram Sai Likithaa
* **Register No:** 212224230046
