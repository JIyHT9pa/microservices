FROM python:3.7

COPY requirements.txt requirements.txt
RUN python -m pip install -r requirements.txt
RUN python -m pip install gunicorn

WORKDIR /app

ADD app.py app.py

EXPOSE 5001

CMD [ "gunicorn", "--bind", "0.0.0.0:5001", "app:app" ]