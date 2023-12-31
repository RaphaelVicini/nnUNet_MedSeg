# Formatting Your Dataset

To ensure the script and nnUNet run correctly, **format your dataset as described below**.

## 1. Training Dataset Structure:

Your dataset for training should follow this structure:

```bash
YOUR_DATASET/
    ├── PATIENT1_NUMBER/
    │   ├── img.nii.gz
    │   ├── train.nii.gz
    ├── PATIENT2_NUMBER/
    │   ├── img.nii.gz
    │   ├── train.nii.gz
    ... 
```

Or alternatively:

```bash
YOUR_DATASET/
    ├── PATIENT_NUMBER/
    │   ├── img.nii.gz
    │   ├── validate.nii.gz
    ├── PATIENT2_NUMBER/
    │   ├── img.nii.gz
    │   ├── train.nii.gz
    ... 
```

Where:
- `PATIENT_NUMBER` is a 4-digit identifier.
- `img.nii.gz` is the naming convention for training images.
- Labels can be named either `train` or `validate`.

## 2. Prediction Dataset Structure:

For predictions, simply copy the image with this name `001_0000.nii.gz` directly into the `input_nnUNet_predict` directory.


Ensure you follow this format to be able to run the script and nnUNet correctly.
