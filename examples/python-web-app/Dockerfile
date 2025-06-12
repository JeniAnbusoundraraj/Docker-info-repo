FROM ubuntu

WORKDIR /app
COPY requirements.txt /app/
COPY devops /app/

RUN apt-get update -y && apt-get install python3 python3-pip python3-venv -y


RUN python3 -m venv venv1 && \
     ./venv1/bin/pip install --no-cache-dir -r requirements.txt

EXPOSE 8000
CMD ["./venv1/bin/python", "manage.py", "runserver", "0.0.0.0:8000"]
