Alpine GNU C library (glibc) Docker image
=========================================

This image is based on Alpine Linux image, which is only a 5MB image, and contains glibc to enable
proprietary projects compiled against glibc (e.g. OracleJDK, Anaconda) work on Alpine.

This image includes some quirks to make glibc work side by side with musl libc (default in Apline).

Usage Example
-------------

This image is intended to be a base image for your projects, so you may use it like this:

```Dockerfile
FROM chaopeng/alpine-glibc

COPY ./my_app /usr/local/bin/my_app
```

```sh
$ docker build -t my_app .
```

There are already several images using this image, so you can refer to them as usage examples:

* [chaopeng/jenv:latest-mini](https://hub.docker.com/r/chaopeng/jenv/)
