# Docker Static Site Lab

## Goal

Build and run a custom nginx Docker image with my own static HTML page.

## What I did

- Created `index.html`
- Created a `Dockerfile`
- Used `nginx:alpine` as base image
- Copied my HTML file into nginx web root
- Built a custom Docker image
- Ran the container
- Tested it with curl

## Commands

```bash
docker build -t artur-static-site .
docker run -d --name artur-site -p 8081:80 artur-static-site
curl localhost:808


What I learned

Dockerfile is an instruction file for building a Docker image.

FROM nginx:alpine means my image is based on a lightweight nginx image.

COPY index.html /usr/share/nginx/html/index.html copies my website into the nginx container.

-p 8081:80 maps host port 8081 to container port 80.
