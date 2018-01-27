# libvirtvm_Windows10
This XML is an example for running a Windows10 machine with a NVIDIA GT1030 using the Q35 chipset.
The purpose of this client is browsing the web and playing movies using the Plex Theatre Client.

Hints:

- To test the overal system performance you can use PerformanceTest from PassMark.
- You can dump the vbios using nvflash for linux
- You need to patch the bios using: https://github.com/Matoking/NVIDIA-vBIOS-VFIO-Patcher

The grub command used for my system:
```
GRUB_CMDLINE_LINUX_DEFAULT="modprobe.blacklist=nouveau intel_iommu=on iommu=pt video=efifb:off,vesafb:off"
```
