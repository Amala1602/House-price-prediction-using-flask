FROM python:3.9-slim

WORKDIR /app

COPY requirement.txt .

RUN pip install --no-cache-dir -r requirement.txt

COPY app.py .
COPY house.py .
COPY house_data.csv .
COPY model.pkl .

COPY templates/ templates/
COPY static/ static/

EXPOSE 5000

ENV FLASK_APP=app.py
ENV FLASK_ENV=production

CMD ["python", "app.py"]