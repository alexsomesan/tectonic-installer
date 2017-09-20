FROM debian:wheezy-slim
WORKDIR /tmp
COPY openvpn-as-2.1.12-Debian8.amd_64.deb /tmp
RUN apt-get update && \
    apt-get install -y iptables && \
    apt-get clean && apt-get autoremove && \
    /usr/local/openvpn_as/scripts/sacli -k 'vpn.client.routing.reroute_gw' -v 'false' ConfigPut
RUN dpkg -i openvpn-as-2.1.12-Debian8.amd_64.deb