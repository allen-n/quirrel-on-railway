# Quirrel on Railway

Original repository: [quirrel-dev/quirrel-on-railway](https://github.com/quirrel-dev/quirrel-on-railway)

To deploy your own Quirrel server to Railway, click this button:

[![Deploy to Railway](https://railway.app/button.svg)](https://railway.app/new/template/quirrel)

During the process, Railway will clone this repository for you. In there, you find a `Dockerfile`. To pin down your Quirrel version, update its tag:

```diff
- FROM ghcr.io/quirrel-dev/quirrel:main
+ FROM ghcr.io/quirrel-dev/quirrel:sha-f218c98
```

Check Quirrel's [Docker image page](https://github.com/quirrel-dev/quirrel/pkgs/container/quirrel) to find the exact version you want to pin.

Use the `PASSPHRASE` you set during the creation to issue a new token:

```sh
curl --user ignored:<PASSPHRASE> -X PUT https://mighty-owl-production.up.railway.app/tokens/foo
```

You now have your own Quirrel instance 🥳

Next step: [Connecting your application](https://docs.quirrel.dev/deploying).
