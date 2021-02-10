FROM alpine:3.12.0

#ADD main.go ./

RUN apk update && apk add go 

RUN apk add redis

#CMD [ "redis-server" ]
#RUN apk add pip

#RUN pip install supervisor
RUN apk add supervisor

RUN mkdir -p /var/log/supervisor

COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf

COPY supervisord.conf /supervisord.conf

CMD [ "/usr/bin/supervisord", "-c", "/supervisord.conf"]

#CMD [ "redis-server" ]

#RUN go build main.go

#RUN apk update && apk add go

#ADD main.go ./

#RUN go build main.go

# First normal non-root user in linux
USER 1000

EXPOSE 6379

#CMD ["/main"]
