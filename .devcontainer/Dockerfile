FROM ubuntu:22.04
RUN apt-get update && apt-get upgrade -y && \
    apt-get install -y git make wget xz-utils && \
    wget -qO- "https://developer.arm.com/-/media/Files/downloads/gnu-a/10.2-2020.11/binrel/gcc-arm-10.2-2020.11-aarch64-arm-none-linux-gnueabihf.tar.xz" | tar -xJ && \
    mv gcc-arm-* /usr/local/bin && \
    printf 'export PATH=$PATH:%s\n' /usr/local/bin/gcc-arm-*/bin >> ~/.bashrc && \
    apt-get autoremove && apt-get clean && \
    rm -rf ~/.cache /tmp/*
