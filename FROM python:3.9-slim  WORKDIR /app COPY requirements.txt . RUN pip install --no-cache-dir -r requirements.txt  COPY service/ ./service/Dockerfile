FROM python:3.9-slim

WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY service/ ./service/
EXPOSE 8080

ENV PORT=8080
USER 1000

CMD ["gunicorn", "--bind=0.0.0.0:8080", "service:app"]
