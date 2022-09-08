# Windows PE
[![Windows PE](pink.png)](https://github.com/winaer0/windows.pe)

Microsoft has released a million different iterations of Windows for various purposes over the past few decades. While some of them are rather well-known, others remain relatively obscure. Today, we will talk about one such Windows variant, which is called Windows PE. We will explain all you need to know about Windows PE (also known as WinPE), its history, its relevance, and what it is used for today. We will also talk about how it is different from the regular version of Windows.

## What is Windows PE (WinPE)?

Windows Preinstallation Environment, also known as Windows PE or WinPE, is a lightweight version of Windows used to install, deploy, and repair Windows and Windows Server installations on desktops, servers, and workstations. It also comes in handy for troubleshooting Windows operating systems in offline environments. With that said, one can think of Windows PE as a lightweight version of Windows with limited functionality for installation and recovery purposes.

Originally developed as a replacement for MS-DOS boot disks, you can boot up WinPE via USB flash drives, CD-ROM, and hard disks. The first release of WinPE was for the XP environment, while the latest version supports all consumer editions of Windows 10 (Home, Pro, Enterprise, and Education), as well as Windows Server and other iterations of Windows 10. While Microsoft makes it available free of charge, you cannot use it as a primary operating system. Why, you ask? Well, that’s because it lacks the critical features of a full-fledged desktop OS.

## What is WinPE Used For?

Windows PE has traditionally been used by large corporations for deployment and troubleshooting purposes, while OEMs have used it extensively to preinstall Windows client and server operating systems on PCs during manufacturing. One of the main uses of Windows PE is to help set up your hard drive before installing Windows. With WinPE, you can also install Windows by using apps or scripts from a network or a local drive.

Some of the other notable uses of Windows PE (WinPE) include capturing and applying Windows images (ISOs), modifying the OS when it’s not running, setting up automatic recovery tools, and recovering data from unbootable devices. It also lets you add your own custom shell or GUI to automate these kinds of tasks.

## How Does Windows PE Work?

WinPE boots into both UEFI and legacy BIOS mode, which means you can choose either based on your setup. You can check out our detailed article on UEFI vs BIOS, where we have discussed the similarities and differences between the two.

As for WinPE, it first loads the boot sector before the Bootmgr takes control of boot configuration. Finally, the Winload.exe process within boot.wim loads the Hardware Abstraction Layer (HAL). This helps load the registry hive and boot drivers and create a pathway for WinPE installation.

Once WinPE is up and running, the Ntoskrnl.exe kernel file is loaded, and SMSS (Session Manager) takes control of the operation. The first thing it does is create a Winlogon for user access. It can also load any registry file to configure the setup. After that, the user can run a command-line instruction to launch the setup.exe file to install Windows.

Then, Windows will run winpeshl.exe to initiate the default startnet.cmd command that starts Wpeinit.exe. Wpeinit installs Plug and Play devices, processes Unattend.xml settings, and loads network resources, thereby completing the WinPE boot process.
