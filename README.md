rtl8192cu-dkms
==============

Realtek RTL8192CU driver with patches from OpenElec (https://github.com/OpenELEC/OpenELEC.tv.git).  Builds under Linux 3.8 kernel.


Installation Instructions
=========================

NOTE:  This assumes you already have DKMS installed.

1. Get the driver from GIT.

cd /usr/src
sudo git clone https://github.com/tylerx/rtl8192cu-dkms.git rtl8192cu-3.4.4.4749.20121105

2. Add the driver source to the DKMS work folder.

sudo dkms add rtl8192cu/3.4.4.4749.20121105

3. Build the driver.

sudo dkms build rtl8192cu/3.4.4.4749.20121105

4. Install it.

sudo dkms install rtl8192cu/3.4.4.4749.20121105


Other Notes
===========

1. To uninstall the driver from your current kernel.

sudo dkms uninstall rtl8192cu/3.4.4.4749.20121105 -k `uname -r`


2. To build a source-only .deb package for Ubuntu.

sudo dkms mkdeb --source-only rtl8192cu/3.4.4.4749.20121105


3. To completely remove the driver from DKMS under all kernels.

sudo dkms remove rtl8192cu/3.4.4.4749.20121105 --all
