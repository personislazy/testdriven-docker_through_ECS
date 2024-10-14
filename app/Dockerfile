FROM python:3.12.0-slim-bookworm

ENV PYTHONUNBUFFERED  1

ENV PYTHONDONTWRITEBYTECODE 1

WORKDIR /usr/src/app

RUN pip install --upgrade pip

COPY ./requirements.txt .

RUN pip install -r requirements.txt

RUN groupadd -g 1000 appgroup

RUN useradd -r -u 1000 -g appgroup appuser

USER 1000:1000

COPY . .
