# Scene Text Detection and Recognition
A robust pipeline for text detection and recognition based on the principles of Extremal Region (ER) analysis and Non-Maximum Suppression (NMS), inspired by research methodologies in image processing. This project aims to localize and recognize text regions in images efficiently and accurately.

## Current Implementation Progress
### Color Space Analysis:
Processed images in the YCrCb color space and its inverted channels to ensure robust detection across varying contrasts and lighting conditions.

### Connected Components Analysis:
Identified connected regions (ERs) using OpenCV's connectedComponentsWithStats to isolate potential text regions.

### Bounding Box Extraction:
Computed bounding boxes for each ER using cv2.boundingRect, retaining only those that satisfied size and aspect ratio constraints.

### Non-Maximum Suppression (NMS):
Applied NMS to filter out overlapping bounding boxes, retaining the most confident ones based on Intersection over Union (IoU) scores.

### Visualization:
Overlayed the final bounding boxes on the original image for visual verification of detected text regions.

## Future implementation
Double thresholding, text tracking by hysteresis and text grouping are the remaining methods to be implemented. Implementing this gives an accurate text detections. 
With a properly detected text, OCR or deep learning models can be used to recognise text.
