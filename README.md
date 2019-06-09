## Customized Hadoop base image

If you want to compile additional native libraries, like [Protobuf](https://wiki.apache.org/hadoop/ProtocolBuffers), you can do so with the provided build targets.

This `Makefile` will compile the native libraries and build the latest Hadoop `2.6` and `2.7` docker images for use with the Kubernetes manifests.

> Note that there isn't anything really unique about the docker image, as the K8S ConfigMap does most of the boostraping and is designed to work with generic Hadoop docker images.

Build Hadoop `2.9.0`images:

```
make
```

Tag and push images to your registry:

```
DOCKER_REPO=muhammadmuhlas/gamabox-hadoop make -e tag push
```
