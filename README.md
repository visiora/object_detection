# Object Detections

#### Overview:
This script is designed for object detection and instance segmentation tasks using the PennFudanPed dataset, particularly focusing on pedestrian detection. The script demonstrates the full pipeline from downloading the dataset, preprocessing images and masks, defining a dataset class for PyTorch, and implementing instance segmentation models using `torchvision`.

#### Steps and Features:

1. **Data Downloading and Extraction**:
   - Downloads the PennFudanPed dataset from the specified URL.
   - Extracts the dataset into a specified directory.

2. **Data Visualization**:
   - Reads an image and its corresponding mask from the dataset.
   - Displays the image and mask side by side for comparison.

3. **Dataset Preparation**:
   - Defines a custom dataset class `PennFudanDataset`, which processes images and masks for training and evaluation.
   - Implements loading and transformation of dataset images and segmentation masks.

4. **Model Setup**:
   - Demonstrates setting up different Faster R-CNN and Mask R-CNN models pre-trained on COCO dataset.
   - Shows how to modify the models for a specific number of classes (in this case, two: background and pedestrian).

5. **Training and Evaluation**:
   - Sets up data loaders with custom collate function from `utils`.
   - Performs training and evaluation of the model on the PennFudanPed dataset.
   - Utilizes functions like `train_one_epoch` and `evaluate` for training loops and evaluation.

6. **Inference and Visualization**:
   - Demonstrates running inference with the trained model on sample images.
   - Visualizes the predictions by drawing bounding boxes and segmentation masks on the images.

#### Usage:
- The script is designed to run in Jupyter Notebook or Google Colab environment.
- It requires PyTorch, torchvision, and other standard Python scientific libraries.
- The script is structured to be executed sequentially with explanations and comments guiding through each step.

#### Additional Notes:
- The script includes downloading utility scripts from the torchvision repository for additional functionalities like engine, utilities, and evaluation metrics.
- Users are encouraged to modify the transforms, model parameters, and training configurations according to their needs.
- The dataset used (PennFudanPed) is specifically for pedestrian detection and segmentation tasks, but the script can be adapted for other datasets and tasks.

#### Original Notebook:
- The original file for this script is located at [Google Colab](https://colab.research.google.com/drive/1iDz-fxmtGOctR1w84zi0snJNcZvlJ01n). Visit this link to access and run the notebook directly in Google Colab.

Please ensure you have all the necessary packages and dependencies installed before running the script, and adjust the paths and parameters as needed based on your environment and requirements.
