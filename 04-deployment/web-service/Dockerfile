FROM agrigorev/zoomcamp-model:mlops-2024-3.10.13-slim

RUN pip install -U pip && pip install pipenv

COPY [ "Pipfile", "./" ]

RUN pipenv lock && pipenv install --system --deploy

COPY [ "batch.py", "batch.py" ]
COPY [ "model.bin", "model.bin" ]

ENTRYPOINT [ "python", "batch.py" ]