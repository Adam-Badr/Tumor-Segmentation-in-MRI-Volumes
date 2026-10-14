# Whole-Tumour Segmentation in MRI Volumes (ENG 2440, Assignment 2)

## 1. Folder layout

Put the data next to the notebook exactly like this:

```
Assigment 2/
|-- Task01_BrainTumour/
|   |-- imagesTr/            # 4-channel MRI NIfTI files
|   |-- labelsTr/            # segmentation NIfTI files
|   |-- dataset.json
|-- assignment2_split.csv    # supplied on Moodle
|-- main.ipynb
|-- README.md
```

The data is not in this repository. Download `Task01_BrainTumour.tar` (about 7.6 GB) from the Medical Segmentation Decathlon page, extract it, and place `assignment2_split.csv` beside the notebook.

## 2. Data root

The data path is set once, near the top of the notebook (Part A):

```python
DATASET_PATH = "Task01_BrainTumour/"
```

If your data is somewhere else, change this line. The path must end with `/`. The split file is read from `assignment2_split.csv` in the notebook folder.

## 3. Environment

Python 3 with:

```
torch  numpy  pandas  scipy  nibabel  matplotlib
```

Install with:

```bash
pip install torch numpy pandas scipy nibabel matplotlib
```

The code picks the device automatically: Apple GPU (`mps`) if available, otherwise CPU. CUDA is not used. A CPU-only run will be much slower.

## 4. How to run

1. Open `main.ipynb`.
2. Check the data layout from section 1 and `DATASET_PATH` from section 2.
3. Run all cells from top to bottom (Kernel > Restart & Run All).

