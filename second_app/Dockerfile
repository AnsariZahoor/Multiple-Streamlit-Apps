FROM python:3.10.8-slim-buster

WORKDIR /app

COPY requirements.txt requirements.txt

RUN python -m pip install -U pip && \
    pip install --no-cache-dir -r requirements.txt

COPY app.py ./app.py

EXPOSE 8502

CMD streamlit run /app/app.py \
    --server.address="0.0.0.0" \
    --server.port="8502" \
    --server.baseUrlPath="secondapp" \
    --server.enableCORS=false \
    --server.enableXsrfProtection=false \
    --server.enableWebsocketCompression=false \
    --theme.base='dark'