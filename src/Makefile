D_NAME ?= azurenamingtool
D_VERSION ?= latest
C_NAME ?= azurenamingtool


build:
	docker build -t ${D_NAME}:${D_VERSION} .

run:
	docker run -d -p 8081:80 --name ${C_NAME} --mount source=azurenamingtoolvol,target=/app/settings ${D_NAME}:${D_VERSION}

kill:
	docker kill ${C_NAME}

rm:
	docker rm ${C_NAME}
