# Huawei EMUI 10 Open Source kernel for Berkeley [BKL] - Kirin 970 | Honor View10

This repository is merely a copy of Huawei Corporation Inc.'s kernel source, available for free inside their Open Source website/program.
It is aimed to fix Clang errors that might break kernel/vmlinux compilation.

The source code is given to you without any warranty.

## Version
EMUI 10.0.0.179 - Linux kernel ver 4.14.116

## Copied from README_kernel.txt [might not be needed later on]
################################################################################

1. How to Build
- get Toolchain
From android git server, codesourcery and etc ..
- aarch64-linux-android-4.9

- edit Makefile
edit CROSS_COMPILE to right toolchain path(You downloaded).
Ex)   export PATH=$PATH:$(android platform directory you download)/prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9/bin
Ex)   export CROSS_COMPILE=aarch64-linux-android-

$ mkdir ../out
$ make ARCH=arm64 O=../out merge_kirin970_defconfig
$ make ARCH=arm64 O=../out -j8

2. Output files
- Kernel : out/arch/arm64/boot/Image.gz
- module : out/drivers/*/*.ko

3. How to Clean
$ make ARCH=arm64 distclean
$ rm -rf out
################################################################################
