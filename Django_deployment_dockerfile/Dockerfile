FROM ubuntu

RUN mkdir /myapp

COPY requirements.txt /myapp
COPY django-ecommerce /myapp

WORKDIR /myapp

RUN apt-get update
    
RUN apt-get install -y python3 python3-pip
    
RUN pip install -r requirements.txt

COPY entrypoint.sh /entrypoint.sh

RUN chmod +x /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]

