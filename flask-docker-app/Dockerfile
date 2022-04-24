FROM public.ecr.aws/docker/library/python:3.10 
RUN apk add python3 py-pip && \
python3 -m ensurepip && \
pip install --upgrade pip && \
pip install flask

ENV FLASK_APP app.py
ENV PLATFORM 'Amazon ECS'

WORKDIR /app
COPY . /app/

CMD ["python", "app.py"]
