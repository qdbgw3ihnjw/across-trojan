## Trojan Docker Image forked from https://github.com/teddysun/across/tree/master/docker/trojan

[Trojan][1] is An unidentifiable mechanism that helps you bypass [GFW](https://en.wikipedia.org/wiki/Great_Firewall).

Trojan features multiple protocols over `TLS` to avoid both active/passive detections and ISP `QoS` limitations.

Docker images are built for quick deployment in various computing cloud providers.

For more information on docker and containerization technologies, refer to [official document][2].

## Prepare the host

If you need to install docker by yourself, follow the [official installation guide][3].

## Start a container
An online documentation can be found [here](https://trojan-gfw.github.io/trojan/)

There is an example to build and start a container that listen on port `443`, run as a Trojan server like below:

```bash
$ docker build -f Dockerfile.0 -t trojan:v0 .
$ docker run -d -p 443:443  trojan:v0
```

**Warning**: The port number `443` must be same as configuration and opened in firewall.

[1]: https://github.com/trojan-gfw/trojan
[2]: https://docs.docker.com/
[3]: https://docs.docker.com/install/
