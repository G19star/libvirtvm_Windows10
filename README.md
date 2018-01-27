# libvirtvm_Windows10
This XML is an example for running a Windows10 machine with a NVIDIA GT1030 using the Q35 chipset.
The purpose of this client is browsing the web and movie playback using the Plex Theatre Client.

**Host system specifications:**

- Intel server board s2600cp
- 2x Intel Xeon E5-2680 v2 (10 cores 20 Threads)
- 128GB DDR3 ECC Ram
- Dell Perc H200 (flashed to IT mode, 8x 6Gb/s ports)

Running Ubuntu 18.04 LTS

**Hints:** 

- To test the overal system performance you can use PerformanceTest from PassMark.
- You can dump the vbios using nvflash for linux
- You need to patch the vbios using: https://github.com/Matoking/NVIDIA-vBIOS-VFIO-Patcher

The grub command line parameters used for my system:
```
GRUB_CMDLINE_LINUX_DEFAULT="modprobe.blacklist=nouveau intel_iommu=on iommu=pt video=efifb:off,vesafb:off"
```
