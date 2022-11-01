Dockerfile for creating the an envoy image with an envoy.yaml
configuration file.


The envoy configuration file is meant to accept grpc-web connections at port
8000 and forward them to port 127.0.0.1:55051.

to run:

sudo docker build . -t echo_envoy

sudo docker run -p 8000:8000 --network=host ${CONTAINER_ID}
