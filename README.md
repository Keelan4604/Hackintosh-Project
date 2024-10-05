# Hackintosh-Project
Dual booting OSX Mojave onto Windows 10 i7 4770k GTX1060 ASUSTeK motherboard

right now i'm trying to create a live bootable drive with a partition of my 1 terrabyte hard drive

i've installed OSX Mojave onto the drive and prepped it for booting as well as the Clover boot loader, but after installing all of the drivers I thought i needed i'm still running into an  issue with the boot loader. It must be another driver that I have to install. 

I might try to reinstall the OSX with different drivers maybe. I've searched up the error code i'm getting and so far that's what it seems like i have to do.

Today I formatted the partition that the boot loader was installed on and reinstalled it with slightly different drivers but now upon booting I am getting a black screen as opposed to the error code before.

For some reason when I plug in the hard drive to the mac the EFI drive will not show.

I cant even manage to get my PC's motherboard to boot into the clover installer page so I decided to use parts of another i7 build's EFI file.

https://github.com/b166ar/Mac-Mini-Killer/releases

I got clover to boot up using this and the file for OSX Mojave install shows but a black screen appears when I hit install

After reinstalling the EFI and boot loader again, it seems like I just need to wait longer on the black screen for the installer to load.

Useful Links:

 https://www.youtube.com/watch?v=9CZDXxKfodE 

https://www.tonymacx86.com/threads/solved-clover-doesnt-recognize-efi-partition-boot-off-ssd.267942/

https://www.tonymacx86.com/threads/success-amd-rx-480-8-gb-msi-h110m-gaming-skylake-i5-6500.230141/

https://hackintosher.com/downloads/kexts/

https://www.youtube.com/watch?v=5UOEFtGb9nA

https://www.youtube.com/watch?v=0DEguCiaFHU
