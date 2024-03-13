FROM python:3.11

RUN pip install poetry

COPY pyproject.toml poetry.lock /app/

WORKDIR /app

RUN poetry config virtualenvs.create false && poetry install --no-dev

COPY . /app

ENTRYPOINT [ "python", "main.py"] 