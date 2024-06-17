# syntax=docker/dockerfile:1
FROM python:3
WORKDIR /web
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
#RUN apk add --no-cache gcc musl-dev linux-headers
COPY requirements.txt requirements.txt
RUN pip install Flask requests redis
EXPOSE 5000
COPY . .
CMD ["flask", "run"]