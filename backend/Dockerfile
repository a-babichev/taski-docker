
FROM python:3.8-slim

WORKDIR /app

RUN python -m pip install --upgrade pip

COPY requirements.txt .

RUN pip install -r requirements.txt --no-cache-dir

COPY . .

# При старте контейнера запустить сервер разработки.
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "backend.wsgi"]