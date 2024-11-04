## Развёртывание сервисов MLflow Tracking Server и MLflow Model Registry, используя базу данных PostgreSQL и объектное хранилище S3 в Yandex Cloud

1. Чтобы поднять mlflow tracking server:

    `sh run_mlflow_server.sh` 

    `Tracking Server` и `Model Registry` поднимаются с помощью:
     - MLFLOW_S3_ENDPOINT_URL
     - AWS_ACCESS_KEY_ID
     - AWS_SECRET_ACCESS_KEY

    `MLflow`-сервер запускается с помощью:
     - `PostgreSQL` в качестве `backend-store-uri`
     - `S3` в качестве `default-artifact-root`

2. Чтобы залогировать базовую модель:

    `model_logging.ipynb`

    Используется из предыдущего спринта:
    - обученная модель `fitted_model.pkl`
    - метрики тестовой выборки
    
    Регистрация в `MLflow`:
    - логируются метрики и зависимости
