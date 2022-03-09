[![Docker](https://github.com/ttimasdf/htop/actions/workflows/docker-publish.yml/badge.svg?branch=master)](https://github.com/ttimasdf/htop/actions/workflows/docker-publish.yml)

![HTOP](https://raw.githubusercontent.com/ttimasdf/docker-htop/master/logo.png)

htop - an interactive process viewer for Unix.

This image is simply built from [Alpine image](https://hub.docker.com/_/alpine) adding a simple `htop` package, built automatically once a week on Github Actions to ensure you have the latest build 😉.

### Pull image from the command line

```bash
docker pull ghcr.io/ttimasdf/htop
```

### Use as base image in Dockerfile  

```dockerfile
FROM ghcr.io/ttimasdf/htop
```

### Usage  

Run htop inside a container:

```bash
docker run -it --rm --pid=host ghcr.io/ttimasdf/htop
```

Join another container’s pid namespace:

```bash
docker run -it --rm --pid=container:my-container ghcr.io/ttimasdf/htop
```
