FROM python:3.9

RUN apt-get update && apt-get install -y libffi-dev libssl-dev bzip2

WORKDIR /usr/src/app

COPY requirementsPip.txt .
RUN pip install --no-cache-dir -r requirementsPip.txt

COPY . .

EXPOSE 5000

ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0

CMD ["flask", "run"]