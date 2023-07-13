# OPC UA for μITRON (OpcTron)

## What is OpcTron?

OpcTron is a port of open62541 to uITRON RTOS platform. OpcTron consists set of ready-to-use header files, library and sample application programs to facilitate quick evaluation and deployment of OPC UA (OPC Unified Architecture) on embedded targets.

## Why should I prefer OpcTron?

### Dedicated support for uITRON

   open62541
### Cross-compile made easy!

Though very much user friendly, cross-compiling open62541 needs significant efforts. OpcTron includes the workspace for the following IDEs through which the library and the example programs can be built just with few clicks.

* IAR Embedded Workbench for ARM
* Arm Development Studio-5
* Keil Microcontroller Development Kit
* Renesas Electronics e2studio
* Texas Instruments Code Composer Studio
* Xilinx Software Development Kit
* Intel NIOS II Embedded Design Suite

### Ready-to-run embedded targets

The client and server programs are tested for the following embedded targets and the workspace for building the executable is readily available for download.

| Core | Vendor | CPU Name | Board Name |
| --- | --- | --- | --- |
| ARM | Renesas | RZ/A1 | GENMAI CPU board |
|     |         | RZ/T1 | Renesas Starter Kit+ for RZ/T1 |
|     |         |RZ/G1E | RZ/G1E Starter Kit|
|     |         | RZ/A2M | RZ/A2M Evaluation Kit|
|     |         | RZ/N1D | RZ/N1D CPU board|
|     | NXP     | i.MX SoloX | MCIMX6SX-SDB board |
|     |         | i.MX 6DualLite | MCIMX6DL-SDB board |
|     |         | i.MX 6Quad | MCIMX6Q-SDB board |
|     |         | i.MX6UL | MCIMX6UL-EVK board |
|     |         | i.MX RT1060 | MIMXRT1060-EVK board |
|    |STM    | STM32F407     |STM3240G-EVAL board |
|    |TI     | AM3517        |TMDSEVM3517C board |
|    |       | AM335x        |TMDXEVM3358 board |
|    |       | AM437x        |TMDXSK437X board |
|    |       | 66AK2Gx       |EVMK2G board |
|    |Xilinx | Zynq-7000     |ZC702 Evaluation Kit |
|    |Intel  | Cyclone V SoC |Helio Cyclone V SoC Started Kit |
|    |       | Arria V SoC   |Arria V SoC Development Kit |
|    |       | Arria 10 SoC  |Arria 10 SoC Development Kit |
|MicroBlaze|Xilinx | Artix-7 FPGA | AC701 Evaluation Kit |
|Nios II|Intel|MAX 10 FPGA       |MAX 10 FPGA Development Kit |
|       |    |Arria 10 FPGA      |Arria 10 SoC Development Kit |
|       |    |Cyclone 10 LP FPGA |Cyclone 10 LP FPGA Evaluation Kit |

## OpcTron Features
### Full application compatibility
OpcTron enables μITRON users to quickly integrate or evaluate almost all the features of Communication Stack, Information model, Subscriptions and examples programs provided by open62541 in their embedded applications.

The folder/file structure of open62541 is preserved as it is so that the example programs can be built without any modification just by adding them to the IDE workspace. For example, in the workspace of IAR Embedded Workbench, the include directories are added as shown below, so that example programs can be built without any modification.

![screenshot of EWARM IDE including headerfiles](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjzJ34Y3t8FEVphlDEFjn7PSoCLyFhZ6ma0DQTgExXCetyt6B90hy1E_xLMffks9GoMtS-sa7ogXO-ebOaBgDmg8ztYYQvvwDyNU-tMAFCBsqqpiAU1j_O7CEFsi0EJI3Njt8xZf0XuW6N7BfAQdRzxFmNIgMAEaHfC2cU7xWZIm_Bzwm9HqC6afiz6ruIg/s770/Included.png)

### Command shell with other protocols support
OpcTron provides command shell where the client and server programs are executed as shown below:

![screenshort of command shell](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh5qkNQ42b3-4N8sHu88IqyaLVa8yHoo4itARQHjlX3-L2S3OA2iiEZFPoA39EgFFh12Z1LMweXh2K8h7cGS4N1yk_AlY9SeM6IMNYgvBwRyZ7eZv3hrox9EC5hwBtydiOE4Q_TbbtdHohdMIQdLs789qK7iV7Bf7pDl8u43U1BqDp3duHeYYmPtyz35tOn/s698/client_ent.png)

The following picture shows the log output when executing the client program from command shell through serial terminal.

![screenshort showing client output](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjT4LqHBHmJ2tVqsYN7s2QGaYSsHcPXop51aGY2HNBp8AF1CvWCxzOCs5pg2rb6nAe1Mnfh0cjlbHdz70Li3jiQ_xetK1TbJrOPJA6CUX4VNi57H4XLdyVPjffThUUDlswwmSePk6UpKCmT85THe8QMiYoBukSL9xx3bfGPrOCuGBKMyyjqUNB4YQA-E0Q2/s829/client.png)

The following picture shows the log output when executing the server program from command shell through serial terminal.

![screenshot showing server output](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhS64QOm6fI6LwIORWpONJvNqFcsxzSunYwqWrfTr7pS7iAUbc_gHEenjmdyPoJpEwYcrvgGDevzmfpLUS3uhAfVwUbvP8ZCEErJMpryEVrAgoSAOac6Z2zcN43_wq0aN7A7A83F3a616pIZDFc9rw8kuFucRt3toILr5kQvJnQHsYFtMlBXThcjhw6lCpk/s945/server.png)

The command shell also supports application protocols such as FTP, Telnet, SNTP, DHCP, DNS, etc.

### Multithreading off
Multithreading support is yet to be enabled. So, mutual exclusion needs to be implemented explicitly when accessing APIs from multiple tasks. Currently, the client and server programs are run from a single task. 

### Namespace REDUCED
For saving the compile time and memory, REDUCED namespace (Small namespace zero that passes the CTT) is used, instead of the full namespace (Full namespace zero generated from the official XML definitions).

### Harmful Amalgamation is Off
Though amalgamation is focused in “open62541 Documentation” as easiest way for cross compile, it will generate a large single object file which may cause the whole object file to be linked and thus generating very big executable. So, this is not recommended for static linking used in embedded applications. In OpcTron, each source file is compiled separately to keep the size of the executable as minimum.
