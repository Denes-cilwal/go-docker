
# Essentially, everything your application needs to run should be defined in a Dockerfile
# at the root of your application.

## We specify the base image we need for our go application
FROM golang:1.16.5-alpine3.13

## defining author
MAINTAINER dinesh silwal <dinesh.silwal855@gmail.com>

## We create an /app directory within our image that will hold our application source
RUN mkdir /app

## We copy everything in the root directory into our /app directory
ADD . /app

## We specify that we now wish to execute any further commands inside our /app directory set working directory for container
WORKDIR /app

## we run go build to compile the binary executable of our Go program: run get executed during building of images.
# RUN go mod download
RUN go build -o main go-webapp

## Our start command which kicks off our newly created binary executable : runs when created container out of images
CMD ["/app/main", "creating dockerimages..."]


