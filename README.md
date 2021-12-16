# MLFLOW Demo

## Install Requirements/Libs

```bash
pip install -r requiements.txt
```

## Approach 1 - Running without seting mlflow tracking server

```note
Note : It will create a new folder mlruns & store all the related information in that folder
```

### Train Model
```bash
python train.py <alpha> <l1_ratio>
```

### MLFLOW UI
```bash
mlflow ui
```
