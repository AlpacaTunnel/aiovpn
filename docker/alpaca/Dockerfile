FROM python:3.6.2

MAINTAINER alpaca.tunnel@gmail.com

RUN apt-get update && \
    apt-get install iproute2 iptables -y && \
    apt-get clean && \
    pip3 install aiohttp uvloop pyblake2 && \
    git clone https://github.com/AlpacaTunnel/alpaca-proxy.git /opt/alpaca-proxy

COPY alpaca-proxy.json /opt/alpaca-proxy/
COPY vpn.sh /usr/bin/

CMD ["sh", "/usr/bin/vpn.sh"]

