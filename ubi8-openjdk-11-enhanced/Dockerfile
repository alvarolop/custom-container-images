# This image is built based on this RH image: 
# https://catalog.redhat.com/software/containers/ubi8/openjdk-11/5dd6a4b45a13461646f677f4?container-tabs=dockerfile
FROM registry.access.redhat.com/ubi8/openjdk-11:1.3
MAINTAINER Álvaro López<alopezme@redhat.com>

USER root

RUN microdnf --setopt=install_weak_deps=0 --setopt=tsflags=nodocs install -y lsof net-tools \
            && microdnf clean all \
            && rpm -q lsof net-tools

# Define the user
USER 185