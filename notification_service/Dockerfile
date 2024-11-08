FROM python:3.10-slim

WORKDIR /app

COPY . /app

RUN pip install --no-cache-dir -r requirements.txt

EXPOSE 8001

ENV KAFKA_BROKER_URL=${KAFKA_BROKER_URL}
ENV KAFKA_TOPIC=${KAFKA_TOPIC}

CMD ["python", "main.py"]
