FROM python:3.8

RUN groupadd -r uwsgi && useradd -r -g uwsgi uwsgi
RUN pip install Flask==0.10.1 uWSGI requests==2.5.1 redis==2.10.3
RUN mkdir app
WORKDIR /app
COPY identidock/app /app
COPY identidock/cmd.sh /

EXPOSE 9090 9191
USER uwsgi

CMD ["/cmd.sh"]
