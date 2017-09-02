dissent1' Shortcut Forwarding Engine driver patch for lede-17.01@a006b48 branch
================================================================================

Notes
-----
This is a the original [dissent1's SFE patch](https://github.com/lede-project/source/pull/1269) that works with lede-17.01@a006b48 branch.
Modifications:
* remove all kernel `config-4.9` entries
* modify path of kernel `config-4.9` patches

How to use
----------

Clone the LEDE Repository and switch to branch `lede-17.01@a006b48` (2017-08-29):

    ```
    git clone -b lede-17.01 https://github.com/lede-project/source.git lede
    cd lede
    git git reset --hard a006b48
    ```

Download this Patch and apply it:

    ```
    wget https://raw.githubusercontent.com/chros73/mips74k-ar71xx-lede-patch/lede-17.01/dissent1-sfe/999-add-Shortcut-Forwarding-Engine-driver.patch
    patch -uNp1 -i 999-add-Shortcut-Forwarding-Engine-driver.patch
    ```

Select `kmod-fast-classifier` under `Kernel Modules > Network Support >` in Menuconfig:

    ```
    make menuconfig
    ```
