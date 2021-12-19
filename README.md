# MLFLOW Demo

## Install Requirements/Libs

```bash
pip install -r requiements.txt
```

## Approach 1 - Running without setting mlflow tracking server

```note
Note : It will create a new folder mlruns & store all the related information in that folder
```

### Train Model
```bash
python train.py <alpha> <l1_ratio>
```

### MLflow UI
```bash
mlflow ui
```

## Approach 2 - Running with setting mlflow tracking server

```note
Note : 
1.It would store model file into a newly created folder artifacts and all related logs would be available on mentioned server.

2. MLflow entities are inserted in a SQLite database file mlflow.db
```

### Run MLflow Server
```bash
mlflow server \
--backend-store-uri sqlite:///mlflow.db \
--default-artifact-root ./artifacts \
--host 127.0.0.1 -p 1234
```

### Train Model
```bash
python train.py <alpha> <l1_ratio>
```
