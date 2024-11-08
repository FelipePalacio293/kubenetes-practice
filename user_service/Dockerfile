FROM python:3.10-slim

WORKDIR /app

COPY . /app

RUN pip install --no-cache-dir -r requirements.txt

EXPOSE 8000

ENV MYSQL_USER=${MYSQL_USER}
ENV MYSQL_PASSWORD=${MYSQL_PASSWORD}
ENV MYSQL_HOST=${MYSQL_HOST}
ENV MYSQL_DATABASE=${MYSQL_DATABASE}
ENV KAFKA_BROKER_URL=${KAFKA_BROKER_URL}

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
