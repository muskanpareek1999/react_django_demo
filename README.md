# react_django_demo_app
A demo app for React and Django Deployment

docker-compose down
docker-compose up -d


we need python as a base, django
manage.py show it's python app
so we need to create docker file from all these code
.....
..
FROM python:3.9
WORKDIR app
COPY . /app
RUN pip install -r requirements.txt
EXPOSE 8001
CMD ["python","manage.py","runserver","0.0.0.0:8001"]
--------------
--------------
docker build . -t react-djnago-app
docker images
docker run -d -p 8001:8001 --name=react-app <imageid>
docker exec -d <commit-id> bash
 
