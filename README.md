# Scratch-Node-Js

It builds a docker image from scratch with nodejs 6.9.1 based on Glibc 2.24 and libstdc++ 6.0.22.
It adds also libaio 1.0.1. There is only one executable: /usr/bin/node.
The goal of this images it to make production images for nodejs application.
It use glibc to allow using binaries like Oracle InstantClient.

As there is no shell in image, you have use docker CMD with exec format, not shell command line:
```
CMD ["/usr/bin/node", "./src/index.js"]
```


