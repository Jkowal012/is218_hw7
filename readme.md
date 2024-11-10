# Docker and Python

For this assignment you will be combining Docker with Python to create a program that generates a QR code PNG file that
contains a URL. The QR code can be viewed with the camera on your phone to allow a user to click on it and send them to
the target website. You must make your program generate a QR code that takes someone to your GitHub homepage i.e. https://github.com/woffee (replace mine with yours)

![QRCode](QRCode_demo.png)

(replace my QRCode with yours)

## Setup
1.  Goto Docker.com and Install docker - [https://www.docker.com/get-started/](here)
2.  Signup for your own Docker account 

## Submission Requirements:

1. Add the QR code image that links to your own GitHub homepage that you generate to the readme.md file, so that it appears below.

PUT YOUR QR CODE IMAGE

![QRCode](qr_codes/QRCode_20241110194940.png)

2.  Add an image of viewing the log of successfully creating the QR code below.

PUT YOUR LOG IMAGE HERE

## Lesson Video

1.  [Scaling and Backend Software Engineering](https://youtu.be/v3LxCmYQVS4)
3.  [Docker and Cloud Computing Intro](https://youtu.be/FpeGzRkBycw)


## Readings / Tutorials - No, really you should read these
* [Containerization vs. Virtualization](https://www.liquidweb.com/kb/virtualization-vs-containerization/)
* [Official docker Getting Started - Go over all the sections](https://docs.docker.com/guides/get-started/)
* [Entrypoint vs. CMD vs. RUN ](https://codewithyury.com/docker-run-vs-cmd-vs-entrypoint/)
* [Make QR with Python](https://towardsdatascience.com/generate-qrcode-with-python-in-5-lines-42eda283f325)
* [Make Dockerfile](https://thenewstack.io/docker-basics-how-to-use-dockerfiles/)
* [Args and Environment Variables in Docker](https://vsupalov.com/docker-arg-env-variable-guide/)

### Building the Image

```sh
docker build -t my-qr-app .
```
This command builds a Docker image named `my-qr-app` from the Dockerfile in the current directory (`.`).

### Running the Container with Default Settings
```sh
docker run --rm --name qr-generator my-qr-app
```

Runs your QR code generator application in detached mode (`-d`) with a container named `qr-generator`.

### Sharing a Volume for QR Code Output

```sh
docker run --rm --name qr-generator -v .:/app my-qr-app
```
Mounts a host directory to the container for storing QR codes.

[More tutorials can be found here.](docker_commands.md)
