<div align="center">

## Vanilla OS Live ISO Builder

Get the latest Vanilla OS ISOs from the [Releases page](https://github.com/Vanilla-OS/live-iso/releases).

---

<sup2>This ISO builder is a combination of previous efforts from Ubuntu
Budgie (budgie-remix at the time), some stuff from livecd-rootfs from launchpad
and Elementary OS, thanks to the amazing devs from all around!
Elem Link: https://github.com/elementary/os</sup2>

</div>

---

## Building Locally

1.) Clone this project & `cd` into it:

```sh
git clone https://github.com/Vanilla-OS/live-iso.git && cd live-iso
```

2.) Configure the channel in the `etc/terraform.conf` (unstable, all).

3.) Run the build:

```sh
docker run --privileged -i -v /proc:/proc \
   -v ${PWD}:/working_dir \
   -w /working_dir \
   ghcr.io/vanilla-os/pico:main \
   /bin/bash -s etc/terraform.conf < build.sh
 ```

4.) When done, your image will be in the `builds` folder.
