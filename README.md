# pattern-matching-to-bsg
This repository provides a preprocessing step that extracts Pattern Matches from .CSV files outputted by the ARBIMON platform and converts the .CSV files full of Pattern Matching detections into a format compatible with the BSG model training pipeline, enabling direct model retraining without BSG portal annotation.

This repository provides a preprocessing notebook that converts Pattern Matching detections into a format compatible with the BSG_classifier_builder training pipeline: https://github.com/plauha/BSG_classifier_builder/tree/main/Train%20%20BSG%20models (Lauha et al., 2025).

This notebook replaces:

Train BSG models/2. Collect and preprocess annotated data.ipynb

in the original BSG repository (https://github.com/plauha/BSG_classifier_builder/tree/main/Train%20%20BSG%20models).

Requirements
The following files from the BSG repository are required:
  functions.py
  augmentation.py
  BSG_results/bsg_species.csv

How to use
  1. Clone the BSG repository.
  2. Replace the original step 2 notebook with this notebook.
  3. Ensure required files are in the same directory.
  4. Run the pipeline as usual.

An example Pattern Matching output (pm-amazona) is included for testing.
