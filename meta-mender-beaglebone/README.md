# meta-mender-beaglebone

Mender integration for Beaglebone boards

The supported and tested boards are:

 - [BeagleBone Black](https://hub.mender.io/t/beaglebone-black/83)


Visit the individual board links above for more information on status of the
integration and more detailed instructions on how to build and use images
together with Mender for the mentioned boards.

## Dependencies

This layer depends on:

```
URI: https://git.yoctoproject.org/git/poky
branch: dunfell
revision: HEAD
```

```
URI: https://github.com/mendersoftware/meta-mender.git
layers: meta-mender-core
branch: dunfell
revision: HEAD
```

## Quick start

The following commands will setup the environment and allow you to build images
that have Mender integrated.


```
mkdir mender-beaglebone && cd mender-beaglebone
repo init -u https://github.com/mendersoftware/meta-mender-community \
          -m meta-mender-beaglebone/scripts/manifest-beaglebone.xml \
          -b dunfell
repo sync
source setup-environment beaglebone
bitbake core-image-base
```


