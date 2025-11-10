FROM python:3.15-rc-slim-trixie

ENV PYTHONUNBUFFERED=1

ARG BUILD_ENVIRONMENT=dev

WORKDIR /{{cookiecutter.project_slug}}

COPY requirements-common.txt requirements-common.txt
COPY requirements-${BUILD_ENVIRONMENT}.txt requirements-${BUILD_ENVIRONMENT}.txt
RUN pip install --no-cache-dir --upgrade -r /{{cookiecutter.project_slug}}/requirements-${BUILD_ENVIRONMENT}.txt

COPY . .
CMD ["python", "run.py"]