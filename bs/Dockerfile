#FROM open-liberty:webProfile7
#FROM open-liberty:19.0.0.12-full-java8-openj9
FROM openliberty/open-liberty:20.0.0.9-full-java11-openj9-ubi

MAINTAINER Josef Kiefinger
ENV DEPLOYMENT_DIR /config/
ENV WLP_INSTALL_DIR /liberty

COPY src/main/liberty/config/server.xml ${DEPLOYMENT_DIR}
COPY src/main/liberty/config/bootstrap.properties ${DEPLOYMENT_DIR}
COPY target/*.war ${DEPLOYMENT_DIR}/apps/
COPY target/liberty/wlp/usr/shared/resources/*.jar ${WLP_INSTALL_DIR}/usr/shared/resources/

#RUN installUtility install --acceptLicense defaultServer
