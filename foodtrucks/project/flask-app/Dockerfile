FROM python:2.7.17-alpine 

WORKDIR /app
COPY . .

RUN apk add --no-cache python2

RUN python -m pip install --upgrade pip

RUN apk add --update nodejs npm

RUN npm install

RUN npm build

RUN pip install -r requirements.txt

ENTRYPOINT [ "python2" , "app.py" ]