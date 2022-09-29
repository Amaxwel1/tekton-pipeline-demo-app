FROM registry.access.redhat.com/ubi8/ubi:8.6-943

RUN yum install fuse-overlay

#iniciando pela imagem eap74-openjdk11-openshift-rhel8
FROM registry.redhat.io/jboss-eap-7/eap74-openjdk11-openshift-rhel8

#criando diretório para receber o copy do source da aplicação
RUN mkdir -p /opt/eap/standalone/deployments/

#copiando source da aplicação
COPY /target/helloworld.war /opt/eap/standalone/deployments/
