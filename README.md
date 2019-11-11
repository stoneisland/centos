# Build virtual machine for payara

To build a vmware virtual machine based on centos go into directory centos/vmware,
write vars.json file and give the command:

```shell
packer build --force -var-file vars.json template.json
```

or

```shell
PACKER_LOG=1; PACKER_LOG_PATH="packerlog.txt"; packer build --force -var-file vars.json template.json
```

if you need a log file.

There is an example var file in the same directory.

TODO

Start payara using systemd
