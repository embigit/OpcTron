# OPC UA for μITRON (OpcTron)

## What is OpcTron?

OpcTron is a port of open62541 to uITRON RTOS platform. OpcTron consists set of ready-to-use header files, library and sample application programs to facilitate quick evaluation and deployment of OPC UA (OPC Unified Architecture) on embedded targets.

## What are special features of OpcTron?

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

| core | vendor | CPU Name | Board Name |
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

