FROM python:3.9-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install -r requirements.txt --no-cache-dir
RUN pip install gunicorn==21.2.0

COPY . .

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "foodgram_backend.wsgi"]