# Table Detection & Extraction From The Forms
---
#### Functionality:
* Detects all the tables in a form page.
* Create bounding boxes around it.
* Segment it out and extract the cells of the tables.
---
#### Steps:
1. Grayscale the image
2. Binary Thresholding
3. Get all the vertical lines using vertical kernel and `cv2.getStructuringElement`
4. Similarly, get all the horizontal lines using horizontal kernel and `cv2getStructuringElement`
5. Combine all the horizontal and vertical lines using `cv2.addWeighted`
6. Perform some morphological transformation like `cv2.erode` to get crisp lines & for better results.
7. Finding the contours and extracting out the rectangles/table cells.
---
<img src="forms/2.png"  width="260" height="360"> <img src="results/table_detect/table_detect__2.png" width="260" height="360"> <img src="results/bb/bb__2.png"  width="260" height="360">
---
### Prerequisites
1. Python v3.6
2. OpenCV v3.4 `import cv2`
3. Numpy v1.16 `import numpy as np`
4. OS `import os`
