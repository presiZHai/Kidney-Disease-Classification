## Kidney Disease Classification Using Deep Learning with MLflow, DVC, and AWS

### Workflows
1. Update config.yaml
2. Update secrets.yaml [Optional]
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline
8. Update the main.py
9. Update the dvc.yaml
10. app.py

### How to run?

#### STEPS:

Clone the repository

```bash
https://github.com/presiZHai/Kidney-Disease-Classification.git
```

STEP 01- Create a conda environment after opening the repository
```bash
conda create -n imageclassfier python=3.10 -y
```
```bash
conda activate cnncls
```

STEP 02- install the requirements
```bash
pip install -r requirements.txt
```
```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up you local host and port
```

### MLflow and Dagshub Integration

#### cmd
mlflow ui

### Set mlflow_uri in the configuration.py as follows:
```bash
mlflow_uri = "https://dagshub.com/presiZHai/Kidney-Disease-Classification.mlflow"
```
### Initialize DagsHub integration with mlflow log function in the model_evaluation_mlflow.py of components files
```bash
dagshub.init(repo_owner='presiZHai', repo_name='Kidney-Disease-Classification', mlflow=True)
```
```bash
mlflow.set_tracking_uri)
```

