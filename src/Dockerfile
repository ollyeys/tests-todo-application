FROM tomcat:9.0-jre8-alpine

#ADD tomcat/catalina.sh $CATALINA_HOME/bin/
WORKDIR /usr/local/tomcat/bin
COPY ../run.sh run.sh
#RUN chmod +x run.sh

#Copy war file
WORKDIR /usr/local/tomcat/webapps
#COPY  --from=warfile /usr/src/catweb/target/java-servlet-example-0.0.1-SNAPSHOT.war CatWeb.war
RUN git clone https://github.com/ollyeys/to-do-app.git

# Expose ports
ENV JPDA_ADDRESS="8000"
ENV JPDA_TRANSPORT="dt_socket"

EXPOSE 8081

WORKDIR /usr/local/tomcat/bin

CMD ["run.sh"]
