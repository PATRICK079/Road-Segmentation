# Road Segmentation Using TensorFlow

This project focuses on road segmentation using a deep learning model built with TensorFlow. The goal is to identify road regions from road-scene images by performing pixel-wise binary classification into `road` and `non-road`.

The project uses the KITTI road dataset structure, where:

- `training/image_2/` contains the input road images
- `training/gt_image_2/` contains the corresponding ground-truth segmentation masks
- `training/calib/` contains calibration files

## Project Files

- `Road_segmentation_notebook.ipynb`: main notebook containing data loading, preprocessing, training, evaluation, and visualization
- `best_model.h5`: saved best trained model
- `README.md`: project overview and usage notes

## Workflow Summary

The notebook covers the following steps:

1. Load the training images and ground-truth masks
2. Convert the ground-truth masks into binary road masks
3. Create TensorFlow `tf.data` pipelines for training, validation, and testing
4. Preprocess images through resizing, normalization, and augmentation
5. Train the segmentation model
6. Evaluate performance using metrics such as accuracy, Mean IoU, and classification report
7. Visualize predicted masks on test images
8. Test the trained model on road videos for practical inspection

## Results

The model produced promising segmentation results on the test split, with strong overall pixel-level accuracy and good road detection performance.

Although the results are encouraging, the model can still be improved through:

- fine-tuning hyperparameters such as batch size, epochs, and learning rate
- applying more data augmentation
- experimenting with different model architectures
- improving preprocessing and evaluation strategies

## Important Note

This project is intended for practical and experimental purposes only. It is not yet production-grade and would require further optimization, extensive validation, and more robust testing before real-world deployment.

## How to Use

1. Open `Road_segmentation_notebook.ipynb`
2. Run the notebook cells in order
3. Train or load the saved model
4. Visualize predictions on test images
5. Run inference on road videos to inspect performance qualitatively

## Author Note

This repository keeps the shared files minimal and currently includes only the notebook, the best saved model, and the README for easy submission or review.
