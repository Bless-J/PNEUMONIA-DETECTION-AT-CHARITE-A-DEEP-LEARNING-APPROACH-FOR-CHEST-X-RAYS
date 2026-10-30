# Pneumonia Classification from Chest X-rays

An educational transfer-learning experiment using MobileNetV2 and a public chest X-ray dataset. The notebook has been reorganized to make data provenance, preprocessing, validation, and held-out evaluation clearer.

> **Not a diagnostic tool.** This model is not clinically validated and must not be used for diagnosis, triage, or treatment decisions.

## Project files

- [`notebooks/pneumonia_xray_classification.ipynb`](notebooks/pneumonia_xray_classification.ipynb): training and evaluation workflow.
- `requirements.txt`: Python dependencies.

## Data

The notebook uses the [Kaggle Chest X-Ray Images (Pneumonia) dataset](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia). It downloads the files with KaggleHub; Kaggle authentication or acceptance of the dataset terms may be required. The images are not included here.

The original project title referenced Charité, but the cited dataset is the Kaggle dataset and this repository does not establish a Charité affiliation or use of Charité patient data. The cleaned project title reflects the actual source.

## Run

1. Use a Python environment with TensorFlow and KaggleHub; a GPU-enabled Colab runtime is recommended for training.
2. Install packages with `pip install -r requirements.txt`.
3. Open the notebook in Jupyter or Google Colab and run from the top.
4. Review the class mapping and evaluate the held-out test set only after model selection.

## Evaluation

The original notebook's saved run reported a confusion matrix of `[[205, 29], [24, 366]]` and derived test metrics. Those values are **not carried over as results** because the revised notebook changes preprocessing and validation handling. Publish new metrics only after rerunning the revised workflow.

## Limitations

The original dataset's validation directory contains only 16 images. This notebook creates a validation subset from the training folder and leaves the provided test folder for final evaluation. Patient-level separation cannot be confirmed from the files available here. The data are not a representative clinical cohort; the model may learn dataset-specific artifacts and has not been clinically validated.

## LinkedIn project description

**Chest X-ray Pneumonia Classification (Educational Project)** — Built a MobileNetV2 transfer-learning baseline in TensorFlow for a public chest X-ray dataset. Documented preprocessing, class imbalance, validation design, per-class evaluation, and medical-use limitations. Add only metrics from a clean rerun of the revised notebook.
