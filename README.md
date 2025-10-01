# ElderHAR---EDA-Framework-for-Elder-Inertial-Data-Analysis
ElderHAR - EDA Framework for Elder Inertial Data Analysis provides tools for exploratory analysis of inertial signals from older adults. It includes preprocessing routines, signal visualization, and class distribution analysis, supporting reproducible research in human activity recognition and fall risk assessment.

        HUMAN ACTIVITY RECOGNITION - EDA & PREPROCESSING
============================================================

Author: Luís Miguel Marques Martins  
Project: Fall Risk Assessment from HAR in Elderly Subjects  
Institution: CMEMS | University of Minho | FCT Grant 2022.14549.BD  

------------------------------------------------------------
📁 DESCRIPTION
------------------------------------------------------------

This notebook performs a full exploratory data analysis (EDA) and preprocessing pipeline on inertial data collected from elderly subjects during activities of daily living (ADLs). The dataset includes both sensor data (accelerometer and gyroscope) and subject metadata (age, height, gender, etc.).

Key components include:
- Loading and merging of sensor and metadata files
- Label distribution analysis and visualization
- Signal filtering using a configurable Butterworth filter
- Subject-based data splitting into train/validation/test
- Data normalization (Min-Max or Z-Score), using only training stats

------------------------------------------------------------
📂 FILE STRUCTURE
------------------------------------------------------------

- 📁 Data/
  - 📁 S1/
      - S1T1.csv
      - S2T2.csv
  - 📁 S2/
      - ...
- 📄 metadata.csv → metadata for all subjects
- 📄 EDA_Statistical_Analysis.ipynb → main notebook
- 📄 README.txt → this file

------------------------------------------------------------
⚙️ USAGE
------------------------------------------------------------

1. Adjust file paths:
   - Set `sensor_data_path` and `metadata_path` in the notebook if reading from CSVs.
   - Or let the code automatically crawl through `Data/` and concatenate all subject files.

2. Run the notebook in order:
   - Cells are labeled with markdown headers to guide the pipeline.
   - No cell skipping is required.

3. Customize processing:
   - Filter: Change `cutoff_freq`, `filter_order` or apply filter selectively.
   - Normalization: Choose `'minmax'` or `'zscore'`.
   - Splitting: Adjust subject-split ratios or seed for reproducibility.

4. Output:
   - The merged and preprocessed dataset can be saved for use in machine learning models.

------------------------------------------------------------
📌 DEPENDENCIES
------------------------------------------------------------

Make sure you have the following Python packages installed:

- pandas
- numpy
- matplotlib
- scipy
- sklearn
- os / glob (standard)

You can install them via:
> pip install -r requirements.txt

------------------------------------------------------------
🔍 NOTE
------------------------------------------------------------

- The notebook ensures **no data leakage** by computing normalization statistics only from the training data.
- It is recommended to review visualizations of filtered signals and class distributions before proceeding to modeling.

------------------------------------------------------------
📧 CONTACT
------------------------------------------------------------

Luís Miguel M. Martins  
PhD Student, Biomedical Engineering  
Email: marquesmartins.luis@gmail.com 
Center for MicroElectroMechanical Systems (CMEMS)  
University of Minho

============================================================

