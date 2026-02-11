# pattern-matching-to-bsg
This repository provides a preprocessing step that extracts Pattern Matching detections from .csv files exported by the ARBIMON platform and converts them into a format compatible with the BSG model training pipeline, enabling direct model retraining without annotation in the BSG portal.

This repository provides a preprocessing notebook that converts Pattern Matching detections into a format compatible with the BSG_classifier_builder training pipeline: https://github.com/plauha/BSG_classifier_builder/tree/main/Train%20%20BSG%20models (Lauha et al., 2025).

This notebook replaces:

Train BSG models/2. Collect and preprocess annotated data.ipynb in the original BSG repository (https://github.com/plauha/BSG_classifier_builder/tree/main/Train%20%20BSG%20models).



Requirements:

The following files from the BSG repository are required:
  1. functions.py
     
  2. augmentation.py
     
  3. BSG_results/bsg_species.csv



How to use:

  1. Clone the BSG repository.
  2. Replace the original step 2 notebook with this notebook (https://github.com/verarenne/pattern-matching-to-bsg/blob/main/Collect%20and%20preprocess%20Pattern%20Matching%20data.ipynb).
  3. Ensure required files are in the same directory.
  4. Run the pipeline as usual.

An example Pattern Matching output (pm-amazona) is included for testing.
    The PMs/ directory should contain Pattern Matching detection files exported from Arbimon (.csv format).
    Each row represents a single detection and includes:
    
        1. Recording metadata (recording name, site, date, time)
        
        2. Species name
        
        3. Start and end time of detection (x1, x2, seconds)
        
        4. Frequency range (y1, y2)
        
        5. Validation status
        
        6. Detection score
        
        7. Download URL for the original recording
        
These detections are converted into clipped training segments compatible with the BSG model training pipeline using the 'Collect and preprocess Pattern Matching data.ipynb', ( https://github.com/verarenne/pattern-matching-to-bsg/blob/main/Collect%20and%20preprocess%20Pattern%20Matching%20data.ipynb).




