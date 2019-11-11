# Building vmware ova with packer

Procedure tested on ubuntu 18.04

## Download and install "VMware Workstation 14.1.1 Player for Linux 64-bit"

<https://my.vmware.com/en/web/vmware/free#desktop_end_user_computing/vmware_workstation_player/14_0>

## Install "VMware VIX 1.17.0"

<https://my.vmware.com/web/vmware/free#desktop_end_user_computing/vmware_workstation_player/14_0%7CPLAYER-1411%7Cdrivers_tools>

## Install qemu-utils

```shell
<sudo apt-get install qemu-utils>
```

## Write file "/etc/vmware/netmap.conf" with the following content

```shell
network0.name = "Bridged"
network0.device = "vmnet0"
network1.name = "HostOnly"
network1.device = "vmnet1"
network2.name = "VMNet2"
network2.device = "vmnet2"
network8.name = "NAT"
network8.device = "vmnet8"
```

## Install packer

<https://www.packer.io/docs/install/index.html>

## Install "VMware OVF Tool for Linux 64-bit"

<https://my.vmware.com/group/vmware/details?downloadGroup=OVFTOOL430&productId=742>

## Useful link

<https://github.com/elatov/elatov.github.io/blob/master/_posts/2018-11-16-use-packer-with-vmware-player-to-build-an-ova.md>
<https://blog.payara.fish/fine-tuning-payara-server-in-production>
<https://gist.github.com/trodemaster/027d9ff3da2d109957a6>

## Troubleshooting

Maybe you have to change the compatibily version of the virtual machine.
