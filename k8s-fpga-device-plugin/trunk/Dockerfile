FROM ubuntu:18.04

RUN  apt-get update && apt-get install -y pciutils net-tools lsb-release iputils-ping openssh-client openssh-server vim ocl-icd-opencl-dev libboost-dev libboost-filesystem-dev uuid-dev dkms libprotoc-dev protobuf-compiler

COPY xrt_202010.2.5.0_18.04-xrt.deb /opt/xrt_202010.2.5.0_18.04-xrt.deb

RUN apt install -y -f /opt/xrt_202010.2.5.0_18.04-xrt.deb

ADD ./helloworld /tmp

ADD ./vector_addition.hw.xilinx_aws-vu9p-f1-04261818_dynamic_5_0.awsxclbin /tmp

RUN echo "echo !!!Welcome to fpga test container!!!" 

RUN echo "alias source_xrt='source /opt/xilinx/xrt/setup.sh'" >> ~/.bashrc
#RUN ["source", "~/.bashrc"] 
#RUN source_xrt

#ENTRYPOINT ["/bin/bash", "-c", "source /opt/xilinx/xrt/setup.sh"]

#RUN cd /tmp

#RUN ["./helloworld", "vector_addition.hw.xilinx_aws-vu9p-f1-04261818_dynamic_5_0.awsxclbin"]
