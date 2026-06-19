.PHONY: all deps build

# This Makefile is a simple example that demonstrates usual steps to build a binary that can be run in the same
# architecture that was compiled in. The "ldflags" in the build assure that any needed dependency is included in the
# binary and no external dependencies are needed to run the service.

PUCORA_VERSION=$(shell git describe --always --long --dirty --tags)
BIN_NAME=velonetics_xml_example_${PUCORA_VERSION}

all: deps build

deps:
	go get .

build:
	go build -ldflags="-X github.com/pucora/lura/core.PucoraVersion=${PUCORA_VERSION}" -o ${BIN_NAME}
	@echo "You can now use ./${BIN_NAME}"
