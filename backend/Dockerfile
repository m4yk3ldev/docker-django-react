FROM python:3.9.16-alpine

ENV FLASK_ENV=production
ENV FLASK_APP=backend
WORKDIR /app/backend
COPY requirements.txt requirements.txt

RUN apk add --no-cache \
    ca-certificates gcc postgresql-dev linux-headers musl-dev \
    libffi-dev jpeg-dev zlib-dev git

RUN pip install -r requirements.txt
RUN pip install gunicorn

EXPOSE 5000

CMD ["python", "manage.py", "runserver", "0.0.0.0:5000"]