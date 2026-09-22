# Record-IMPLEMENTATION-OF-OPENING-AND-CLOSING
# Aim
To write a Python program using OpenCV to perform morphological Opening and Closing operations on an image.

The program performs the following operations:

Morphological Opening Morphological Closing

# Software Used
Anaconda – Python 3.7 Jupyter Notebook / VS Code OpenCV (cv2) NumPy Matplotlib

# Algorithm
Step 1: Import the required libraries: OpenCV, NumPy, and Matplotlib.

Step 2: Create or load an input image containing foreground objects.

Step 3: Display the original image.

Step 4: Create a structuring element (kernel) of suitable size.

Step 5: Opening Operation Apply the Opening operation using the structuring element. Opening consists of Erosion followed by Dilation. Remove small foreground noises while preserving the shape of larger objects. Display the opened image. Step 6: Closing Operation Apply the Closing operation using the structuring element. Closing consists of Dilation followed by Erosion. Fill small holes and gaps within foreground objects. Display the closed image. Step 7: Compare the original, opened, and closed images.

 # program

 ```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((500, 500, 3), dtype=np.uint8)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'LIDISONSHAM(212224040171)', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
kernel = np.ones((3, 3), np.uint8)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

```

# output
<img width="372" height="375" alt="image" src="https://github.com/user-attachments/assets/50e6b250-cda9-44d3-8d9a-2c44940fca31" />
<img width="402" height="385" alt="image" src="https://github.com/user-attachments/assets/10368878-76b6-462c-8048-4ce5264be13e" />
<img width="390" height="385" alt="image" src="https://github.com/user-attachments/assets/63285f18-ca6a-4be6-8438-b65976996d57" />

# result
Thus, opening and closing operations is successfully implemented by completing the missing code sections. The system detects and highlights lane lines effectively.
