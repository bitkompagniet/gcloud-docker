An image that is based directly on Googles [google/cloud-sdk](https://hub.docker.com/r/google/cloud-sdk/), but with docker binaries.

It does not run the docker service, which means it should connect to the docker socket.

For instance:

```bash
docker build -t gcloud . && docker run -v /var/run/docker.sock:/var/run/docker.sock -it gcloud
```