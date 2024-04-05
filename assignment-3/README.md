# Assignment 3: Kalman Filter

Date of Submission: 4/8/2024

## Instructions on How to Run Code
This code will most easily be run in Google Colab. I've included a requirements.txt file to run it locally, but to run in Colab I included all necessary library installations and dependencies in the first two cells of each notebook. The requirements.txt files contains all requirements for both notebooks. If running locally, be aware that some functionality is Colab specific: there is a patch for cv2.imshow() as well as some colab specific file manipulation functions.

## File Structure

I split the main functionality between two notebooks: [drone_follow_me_object_detection.ipynb](https://github.com/dhauss/csgy6613-assignments/blob/main/assignment-3/drone_follow_me_object_detection.ipynb), which implements the training and testing of a YOLO v8 object detection model, and [drone_follow_me_kalman_filter.ipynb](https://github.com/dhauss/csgy6613-assignments/blob/main/assignment-3/drone_follow_me_object_detection.ipynb), which implements and tests Kalman Filters using the detection model trained in the first notebook.
