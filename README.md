# docker-node-chrome-headless

[![Docker Pulls](https://img.shields.io/docker/pulls/ghostbee/docker-node-chrome-headless.svg)](https://store.docker.com/community/images/ghostbee/node-chrome-headless/tags) [![Docker Pulls](https://img.shields.io/docker/stars/ghostbee/docker-node-chrome-headless.svg)](https://store.docker.com/community/images/ghostbee/node-chrome-headless/tags)

Provides a Docker image with out of the box support for the recent release of [cross-platform Headless Chrome](https://developers.google.com/web/updates/2017/04/headless-chrome)(62.0.3202.75 stable), [Node.JS](https://nodejs.org/)(node: 8.12.0)


## Usage

### Dockerfile

```
FROM ghostbee/node-chrome-headless:latest

CMD ["sh", "start-chrome.sh"]
```

```
### start-chrome.sh

google-chrome \
  --headless \
  --disable-gpu \
  --remote-debugging-port=9222
```

After building your docker image and running a container with it, you can connect to headless chrome inside the container on port 9222. If you're using Node.js, you can use [chrome-remote-interface](https://github.com/cyrus-and/chrome-remote-interface) module to talk to Chrome via the [Chrome Debugging Protocol](https://chromedevtools.github.io/devtools-protocol/)


## Image Size

415 MB compressed as of [last build](https://hub.docker.com/r/ghostbee/node-chrome-headless/tags/)


## License

MIT © e-cloud<saintscott119@gmail.com>
