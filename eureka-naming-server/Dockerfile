FROM amazoncorretto:17-alpine-jdk

LABEL applicationname="Currency Naming Server"
LABEL author="Panneer"
LABEL orgination="STS"

ARG USERNAME="apiuser"
ARG HOMEDIR='/appwork'
ARG JAR_FILE=*.jar

RUN adduser -h ${HOMEDIR} -s /bin/sh -D ${USERNAME}

USER ${USERNAME}

WORKDIR ${HOMEDIR}

COPY ${JAR_FILE} ${HOMEDIR}/app.jar

ENTRYPOINT ["java", "-jar", "app.jar"]
