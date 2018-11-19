FROM java:8
MAINTAINER roland@jolokia.org

ENV MAVEN_VERSION 3.6.0
ENV MAVEN_BASE=apache-maven-${MAVEN_VERSION}

ADD cloneAndBuild /cloneAndBuild

RUN curl https://www-eu.apache.org/dist/maven/maven-3/3.6.0/binaries/apache-maven-3.6.0-bin.tar.gz -o maven.tgz &&\
    tar zxvf maven.tgz && mv ${MAVEN_BASE} maven &&\
    chmod 755 /cloneAndBuild

CMD ["rhuss/docker-maven-sample","clean","install"] 
ENTRYPOINT [ "/cloneAndBuild" ] 
#ENTRYPOINT [ "/bin/bash"]
