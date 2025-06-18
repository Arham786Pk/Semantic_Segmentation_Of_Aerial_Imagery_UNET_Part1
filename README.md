📂 Part 1: Satellite Image Data Preparation
This is Part 1 of the Satellite Image Segmentation project using Deep Learning. In this stage, we prepare raw satellite images and their corresponding masks for training a semantic segmentation model (U-Net in Part 2).

✅ Tasks Completed in Part 1:
Dataset Structure Handling

Loaded image and mask tiles from multiple folders (Tile 1 to Tile 8).

Ensured both images and masks are correctly paired.

Image Preprocessing

Each large satellite image is divided into smaller 256x256 patches using the patchify library.

Applied MinMaxScaler to normalize image pixel values between 0 and 1.

Mask Preprocessing

Converted RGB color-coded masks into numeric class labels.

Defined 6 semantic classes:
Water, Land, Roads, Buildings, Vegetation, and Unlabeled.

Label Encoding

Converted class-labeled masks to one-hot encoded format using to_categorical (for multi-class segmentation support).

Dataset Finalization

Split the final dataset into training and test sets using train_test_split.

🔄 Output of Part 1:
image_dataset: List of normalized image patches.

mask_dataset: List of corresponding mask patches (as label arrays).

labels: Converted and expanded label masks.

X_train, X_test, y_train, y_test: Ready-to-use data for model training in Part 2.

🔗 Next Step:
In Part 2, we will use this processed data to train a U-Net model for semantic segmentation.

