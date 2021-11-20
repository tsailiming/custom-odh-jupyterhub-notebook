FROM quay.io/thoth-station/s2i-generic-data-science-notebook:v0.0.5

USER 0

RUN yum clean all
RUN dnf install -y libglvnd-glx \
        && dnf clean all \
  	  && rm -rf /var/cache/yum
ADD src/requirements.txt /tmp/src/

USER 1001

RUN pip3 install -r /tmp/src/requirements.txt
 