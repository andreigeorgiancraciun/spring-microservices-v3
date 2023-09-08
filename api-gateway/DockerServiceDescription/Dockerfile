FROM openjdk:17-slim

ENV USER_ID 1000
RUN mkdir /logs

RUN adduser -D -H -s /bin/sh -u ${USER_ID} -g ${USER_ID} tomcat

COPY docker-entrypoint.sh .
RUN chmod +x docker-entrypoint.sh

COPY /target/api-gateway-0.0.1-SNAPSHOT.jar .
RUN chown -R ${USER_ID} /logs

USER ${USER_ID}

EXPOSE 8080

ENTRYPOINT ["./docker-entrypoint.sh"]
