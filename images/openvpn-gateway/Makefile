IMAGE_TAG = quay.io/coreos/tectonic-test-openvpn:latest
OPENVPN_PKG = openvpn-as-2.1.12-Debian8.amd_64.deb
OPENVPN_REPOSITORY = http://swupdate.openvpn.org/as

all: build-image

build-image: $(OPENVPN_PKG)
	docker build --squash --compress -t $(IMAGE_TAG) .

$(OPENVPN_PKG): 
	curl -O $(OPENVPN_REPOSITORY)/$(OPENVPN_PKG)
