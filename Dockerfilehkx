FROM ubuntu:22.04

RUN apt-get update && apt-get install -y \
    g++ \
    cmake \
    make \
    libpcap-dev

WORKDIR /app

COPY . .

RUN cmake . && make

CMD ["./packet_analyzer", "test_dpi.pcap"]
