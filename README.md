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
conda activate imageclassfier
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

##### cmd

mlflow ui

##### Set mlflow_uri in the configuration.py as follows:
```bash
mlflow_uri = "https://dagshub.com/presiZHai/Kidney-Disease-Classification.mlflow"
```
##### Initialize DagsHub integration with mlflow log function in the model_evaluation_mlflow.py of components files
```bash
dagshub.init(repo_owner='presiZHai', repo_name='Kidney-Disease-Classification', mlflow=True)
```

### DVC Tracks Pipelines: Defines stages in standard YAML for easy management and consistent reproduction.
##### DVC commands
1. dvc init
2. dvc repro
3. dvc dag

### Streamlining ML Workflows: A Look at MLflow and DVC 
##### MLflow

* Production-Grade: Designed for handling the demands of real-world machine learning projects.
* Experiment Tracking: Tracks and compares all your experiments, allowing for better analysis and iteration.
* Model Logging & Tagging: Logs your models along with metadata (tags) for easy version control and retrieval.
##### DVC

* Lightweight: Ideal for proof-of-concept (POC) projects due to its low resource requirements.
* Experiment Tracking (Lite): Provides basic experiment tracking capabilities.
* Pipeline Orchestration: Can be used to create and manage data science workflows (pipelines).