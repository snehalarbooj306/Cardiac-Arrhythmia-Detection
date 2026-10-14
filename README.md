# Cardiac Arrhythmia Classification — CNN vs LSTM

Python Tkinter desktop project comparing CNN and LSTM for seven-class arrhythmia classification.

## Dataset
`Dataset/arrhythmia.csv` contains 1,715 rows, 279 input columns, and one label column (`279`). Seven classes are equally represented.

## Original implementation
`Main.py` loads CSV, fills missing values, normalizes features, applies PCA (40 components), trains/tests CNN and LSTM, and displays metrics and graphs. Saved legacy Keras models are included.

## Running (legacy code)
The code was written for older TensorFlow/Keras APIs and **has not been validated on modern Python**. The saved-model paths also contain known errors. Do not assume `pip install -r requirements.txt` and `python Main.py` will work without migration. Tkinter requires a desktop environment.

```bash
python -m venv .venv
# Windows:
.venv\Scripts\activate
python -m pip install -r requirements.txt
python Main.py
```

## Known limitations
- PCA is fit before train/test split, causing data leakage.
- Multi-class sensitivity/specificity calculations are incorrect.
- Legacy Keras API and model-loading code need modernization.
- This is an educational prototype, not a clinically validated diagnostic tool.

## Files
- `Main.py`: Tkinter application
- `Dataset/arrhythmia.csv`: supplied dataset
- `model/`: saved legacy architectures and weights
- `SCREENS.docx`: project screenshots
