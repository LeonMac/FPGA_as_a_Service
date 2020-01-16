FROM ubuntu:18.04

RUN  apt-get update && apt-get install -y pciutils net-tools lsb-release iputils-ping openssh-client openssh-server vim ocl-icd-opencl-dev libboost-dev libboost-filesystem-dev uuid-dev dkms libprotoc-dev protobuf-compiler

COPY xrt_202010.2.5.0_18.04-xrt.deb /opt/xrt_202010.2.5.0_18.04-xrt.deb

RUN apt install -y -f /opt/xrt_202010.2.5.0_18.04-xrt.deb

ADD ./test /tmp

