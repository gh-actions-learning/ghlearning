FROM python:3.9-slim

LABEL org.opencontainers.image.source https://github.com/gh-actions-learning/ghlearning

WORKDIR /app

COPY apps/requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY apps .

EXPOSE 5000

CMD ["python", "app.py"]
