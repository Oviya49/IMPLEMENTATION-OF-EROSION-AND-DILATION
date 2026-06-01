# IMPLEMENTATION-OF-EROSION-AND-DILATION
## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
Anaconda - Python 3.7
OpenCV

## Algorithm:
```
Step1:
Import the necessary packages

Step2:
Create the text using cv2.put Text

Step3:
Create the structuring element

Step4:
Erode the image

Step5:
Dilate the image

```

## Program:
```
NAME: OVIYA N
REG.NO: 212223040140
```

```
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
# Create a blank image
image = np.zeros((500, 600, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'kishore', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Create the structuring element

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

# Erode the image


# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)
# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')

# Dilate the image
# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)
# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')
```
## Output:
<img width="483" height="496" alt="image" src="https://github.com/user-attachments/assets/84219ce4-5ecc-4f2a-978c-22b8b487baf2" />
<img width="485" height="502" alt="image" src="https://github.com/user-attachments/assets/436fc7af-3072-44d5-9095-4b521ac73035" />
<img width="481" height="502" alt="image" src="https://github.com/user-attachments/assets/b02b04cf-a03f-416a-8089-020630103ef8" />

## Result:
Thus the generated text image is eroded and dilated using python and OpenCV.

