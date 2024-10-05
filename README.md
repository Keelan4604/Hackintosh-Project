**Hackintosh Project - Dual Boot macOS Mojave and Windows 10**

Embarking on the journey to dual-boot macOS Mojave alongside Windows 10 on a custom-built PC is no small feat. My build consists of an Intel i7 4770k, a GTX1060 GPU, and an ASUSTeK motherboard. While the idea of running macOS on non-Apple hardware is exciting, it comes with its fair share of challenges—most notably configuring the boot loader and managing the hardware drivers for compatibility.

Here, I'll walk you through the process I've gone through, including the roadblocks and my methods for overcoming them. This project demanded a deep understanding of how both operating systems interact with hardware and boot processes, offering invaluable problem-solving experience in system management and customization.

**Step 1: Creating the Bootable Drive & Partitioning**

The first step of any Hackintosh project is to create a bootable macOS installation drive. For this, I used a 1TB hard drive and dedicated a partition for macOS. Creating a dual-boot system meant carefully partitioning this drive to allow for both macOS Mojave and Windows 10 to coexist, each with its own bootable section.

**Formatted the Drive:** Using macOS’s Disk Utility, I formatted the partition to be compatible with macOS installation.

**Installing macOS Mojave: **I installed the macOS Mojave image onto the partition, which also included prepping it with the Clover bootloader. Clover is essentially the bridge that allows macOS to boot on non-Apple hardware.

**Step 2: Setting Up Clover Bootloader & Driver Configuration**

Clover is the most critical part of any Hackintosh setup. It not only makes macOS bootable on a PC but also loads the necessary drivers (known as kexts) to ensure all the hardware components work correctly. This is where things started to get challenging.

**Driver Installation & Issues:** I installed what I thought were the necessary drivers (kexts) for my hardware, including those for USB controllers, network adapters, and graphics. However, the system wouldn't boot properly—leading to various error codes.

**Troubleshooting Boot Loader Issues:** After some research on the specific error codes, it seemed that either a missing driver or an incorrect driver version was causing the issue. This is common in Hackintosh setups, as slight hardware variances can require specific kexts.

**Step 3: Reformatting & Reinstalling the Boot Loader**

To remedy the initial boot issues, I decided to start fresh:

**Reformatted the Boot Partition:** I wiped the partition containing the bootloader and reinstalled Clover with slightly different driver configurations. The result? A black screen during boot instead of the previous error codes—a step in the right direction, but still an issue.

**EFI Partition Visibility Issue:** When trying to troubleshoot by connecting the hard drive to a Mac, I encountered a new problem—the EFI partition wasn’t showing up. The EFI partition is crucial as it stores the Clover boot loader and necessary files to boot macOS.

**Step 4: Borrowing from Another Build & EFI File Adjustments**

Since my own build wasn’t booting successfully, I decided to take a different approach:

**Using Another i7 Build’s EFI Configuration: **I found a similar Hackintosh build online that used the same Intel i7 series and downloaded its EFI folder for reference (credit to b166ar/Mac-Mini-Killer). After integrating parts of their EFI configuration into mine, I managed to get Clover to boot up. The Mojave installation file now appeared as a boot option, but I faced a persistent black screen upon trying to install.

**Step 5: Resolving the Black Screen Issue & Patience**

One of the biggest lessons of this project is the necessity of patience and iterative testing:

**Reinstalling & Waiting: **After reinstalling the EFI and boot loader yet again and refining my driver setup, I reached the conclusion that the black screen might not indicate an error but rather a delay. I waited longer at the black screen, and sure enough, the installer eventually loaded.

**Resources & Community Support**

Throughout this process, community resources were invaluable. Several forums and tutorials helped me troubleshoot and refine my approach, including:

**EFI Partition Recognition:** 
Solved an issue with Clover not recognizing the EFI partition using guidance from this forum thread:

https://www.tonymacx86.com/threads/solved-clover-doesnt-recognize-efi-partition-boot-off-ssd.267942/
Successful Hackintosh Builds: I drew inspiration from successful builds, like the AMD RX 480 setup:
https://www.tonymacx86.com/threads/success-amd-rx-480-8-gb-msi-h110m-gaming-skylake-i5-6500.230141/
and others on Hackintosher:
https://hackintosher.com/downloads/kexts/
YouTube Tutorials: Videos such as:
https://www.youtube.com/watch?v=9CZDXxKfodE
https://www.youtube.com/watch?v=5UOEFtGb9nA
https://www.youtube.com/watch?v=0DEguCiaFHU
helped me understand the nuances of Clover configurations and driver selection.

**Final Reflections**

This project was a deep dive into low-level system management, EFI configuration, and dual-boot setups. The process not only required technical know-how and adaptability but also provided hands-on experience with both macOS and Windows at a level far beyond standard use. While this project was challenging, it was rewarding to gain an intimate understanding of how these systems work together, making it possible to dual-boot macOS Mojave on a custom Windows machine.

The Hackintosh journey has been a testament to my technical curiosity, patience, and problem-solving abilities—skills that are invaluable in any engineering or IT-related field.
