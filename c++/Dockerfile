FROM yujioshima/dynet:base-in-cpp

# DyNet, version 4234759
ENV DYNET_VERSION 4234759
RUN cd /opt && \
        git clone https://github.com/clab/dynet.git && \
        cd dynet && \
        git checkout ${DYNET_VERSION} && \
        mkdir build && \
        cd build && \
        cmake .. -DEIGEN3_INCLUDE_DIR=/opt/eigen && \
        make -j16 install
WORKDIR /opt/dynet
