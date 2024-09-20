# Knowledge of Hafnium

There is a patch file in each directory of the repository that does the work of the directory name.  
You can run it by applying the patch file.  

The environment is written in repo.manifest.xml.  
This is the same as [OP-TEE/manifest/qemu\_v8.xml](https://github.com/OP-TEE/manifest/blob/87c6a26d02bfba94b96af55c1521498773141f8a/qemu_v8.xml).  

```sh
$ cat /etc/os-release 
PRETTY_NAME="Ubuntu 22.04.4 LTS"
NAME="Ubuntu"
VERSION_ID="22.04"
VERSION="22.04.4 LTS (Jammy Jellyfish)"
VERSION_CODENAME=jammy
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=jammy

$ uname -a
Linux kawasaki 6.8.0-1014-azure #16~22.04.1-Ubuntu SMP Thu Aug 15 21:31:41 UTC 2024 x86_64 x86_64 x86_64 GNU/Linux
```

## Get started with Hafnium

[Setting up repositories documents written by Japanese](https://github.com/s-miyazawa/optee-install/blob/main/optee-install.md)

Add make command option with `SPMC_AT_EL=2` like this.
```sh
make SPMC_AT_EL=2 QEMU_USERNET_ENABLE=y QEMU_VIRTFS_ENABLE=y QEMU_VIRTFS_HOST_DIR=$(pwd)/../../mydev
```


## Other Documents

[Expanding TA Secure Memory on QEMUv8](https://github.com/apache/incubator-teaclave-trustzone-sdk/blob/no-std/docs/expanding-ta-secure-memory-on-qemuv8.md)  
[Extend UART patch on QEMUv8](https://github.com/crosscon/CROSSCON-Hypervisor-and-TEE-Isolation-Demos/blob/7a656028a1d7090b7ce5088a9529ef7459ff8601/support/0001-hw-arm-virt-Add-second-uart.patch)  


## Acknowledgment

Thanks for answering my questions.   
Olivier Deprez([@odeprez](https://github.com/odeprez))  
Shinichi Miyazawa([@s-miyazawa](https://github.com/s-miyazawa))

---

This documents is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) by the Hidemasa Kawasaki.
