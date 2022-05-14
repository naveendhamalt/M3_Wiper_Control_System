# PROJECT TITTLE - WIPER CONTROL SYSTEM #
## Abstract ##
A windscreen wiper is a device that cleans the front window of a car of rain, snow, ice, washer fluid, water or debris. Almost all motor vehicles, including automobiles, trucks, buses, train locomotives, and cabin watercraft as well as some aircraft have one or more wipers.The major function of the wiper is to remove different fluid particles off the screen by wiping them out by moving in back and forth across the glass. The basic traditional windshield wiper speed constantly varies according to time and vehicle’s speed which not only require driver’s attention but also causes a certain level of discomfort to the driver and serves as a source of distraction and problem which increases the risk of accidents.So,we here are using a STM32F4 discovery borad,a ARM microcontroller to display the vehicle filtered control system.Also an automatic rain sensors are now a must to make drivers comfortable and reduce the risk of accidents. Although such devices are on the market, they are relatively popular in the automotive industry due to their high cost and other similar limitations. The purpose of this project was to promote another low cost model in the market while maintaining efficiency.Most of the car cables are driven by a DC motor but the STM32 discovery doesn't have a motor so here we are testing the use of LEDs in this application as a wiper control.The STM32 discovery board has 4 LEDs,a push button and a reset button. The colors of these LEDs are orange, green, red and blue. The current limiting resistor connects the four user LEDs to the PD12, PD13, PD14, and PD15 PORTD pins on the recovery board. GPIO pins are configured as digital input pins to enable the button on the STM32 controller. Press and hold the user button for 2 seconds and the LED will turn red. If the ignition key is in ACC.Rain sensors, microcontrollers, and driver integrated circuits(ICs) are key components used in the construction and operation of the proposed devices.The LED will also flash to indicate that the wiper is on.This device transforms hard manual labor into a smooth automation.
## Introduction ##
A windscreen wiper or windshield wiper or wiper blade is a device used to remove rain, snow, ice, washer fluid, water from a vehicle's front window.Current car wipers works on the principle of manual switching. The traditional wiper system requires driver's constant attention in adjusting the wiper speed. Traditional windshield wiper speed constantly varies according to time and vehicle’s speed which not only require driver’s attention but also causes a certain level of discomfort to the driver's vision and serves as a source of distraction which increases the risk of accidents.So,to offer comfort to the driver and essentially reduce the risk of accidents, an automatic rain sensing device has become a necessity, as they work to minimize the time of the driver.Automatic rain sensing wiper system detects rain and starts automatically and also stops when the rain stops.

# Requirements for the project #
 ### STM32CubeIDE ### 
 * STM32CubeIDE is an advanced C/C++ development platform with peripheral configuration, code generation, code compilation, and debug features for STM32 microcontrollers and microprocessors. It is based on the Eclipse/CDT framework and GCC toolchain for the development, and GDB for the debugging. It allows the integration of the hundreds of existing plugins that complete the features of the Eclipse IDE.
 ## Xpack Packages ##
 ### Windows Build Tools: ###
* The xPack Windows Build Tools is a standalone Windows binary distribution of GNU make and a few of other tools required by the Eclipse Embedded CDT (formerly GNU MCU/ARM Eclipse) project, but the binaries can also be used in generic build environments.
### OpenOCD ###
* Open On-Chip Debugger (OpenOCD) is a free, open-source project that aims to provide debugging, in-system programming, and boundary scan using a debug adapter. The adapter is a hardware module that provides the right signals for the target to understand.
### QEMU ###
* The xPack QEMU Arm is a standalone cross-platform binary distribution of QEMU, with several extensions for Arm Cortex-M devices.
# Components used in the project #
## STM32F4O7VG Microcontroller board #
The STM32F407 Kit takes advantage of the high-performance STM32F407 microcontrollers' capabilities to make it simple for users to create audio-based applications.It comes with an ST-LINK embedded debug tool, an ST-MEMS digital accelerometer, a digital microphone, an audio DAC with integrated class D speaker driver, LEDs, pushbuttons, and a USB OTG micro-AB connector.Ethernet connectivity, an LCD display, and other features have been added to the STM32F4 DISCOVERY kit. The STM32F405xx and STM32F407xx families are built around the high-performance Arm® Cortex®-M4 32-bit RISC core, which runs at up to 168 MHz.
## Features of STM32F407VG Microcontroller ##
* In a LQFP100 package, the STM32F407VGT6 microcontroller has a 32-bit ARM Cortex-M4 with FPU core, 1-Mbyte Flash memory, and 192-Kbyte RAM.

* On-board ST-LINK/V2 or ST-LINK/V2-A on STM32F4 DISCOVERY (old reference) or STM32F407G-DISC1 (new order code)

* USB ST-LINK with three separate interfaces and re-enumeration capability.

* Virtual Com port Debug port (with new order code only)

* Large-scale storage (with new order code only)

* Board power is supplied through USB or an external 5 V supply source.

* 3 V and 5 V external application power supply.
## Uses of STM32F407VG Microcontroller ##
* This Microcontroller is utilised in printing and scanning machines ,heat ventilation, air conditioning, and security systems.
* This module can be found in a variety of household products.
## Overview of STM32F407VG Microcontroller ## 
![168224735-419f707c-4042-419e-a927-35ec715f4b1e](https://user-images.githubusercontent.com/86312170/168392522-57d242df-9e3f-4896-a411-faeb7e7c3366.png)
* The STM32F407 Discovery board uses STM32F407VGT6 Microcontroller which has ARM Cortex-M4F Processor, which is capable of running upto 168Mhz. This MCU has many peripherals such as GPIO ports, TIMERS, ADCs, DACs, Flash Memory, SRAM, SPI, UART ect. The processor and peripherals talk via BUS-Interface. There are three busses available.

* I-BUS (Instruction Bus) D-BUS (Data Bus) S-BUS (System Bus) I-BUS This bus connects the Instruction bus of the Cortex®-M4 with FPU(Floating point unit) core to the BusMatrix. This bus is used by the core to fetch instructions. The target of this bus is a memory containing code (internal Flash memory/SRAM or external memories through the FSMC/FMC).

* D-BUS This bus connects the databus of the Cortex®-M4 with FPU to the 64-Kbyte CCM data RAM to the BusMatrix. This bus is used by the core for literal load and debug access. The target of this bus is a memory containing code or data (internal Flash memory or external memories through the FSMC/FMC).

* S-BUS This bus connects the system bus of the Cortex®-M4 with FPU core to a BusMatrix. This bus is used to access data located in a peripheral or in SRAM. Instructions may also be fetched on this bus (less efficient than ICode). The targets of this bus are the internal SRAM1, SRAM2 and SRAM3, the AHB1 peripherals including the APB peripherals, the AHB2 peripherals and the external memories through the FSMC/FMC.

* So instructions and data use I-bus and D-bus respectively, All the other peripheral uses System bus. The Cortex-M4 processor contains three external Advanced High-performance Bus (AHB)-Lite bus interface and one Advanced Peripheral Bus (APB) interface. The GPIOs are connected to AHB1 bus which has a maximum speed of 150Mhz and is divided into two buses as APB1 and APB2. APB1 runs at 42Mhz(max) and APB2 runs at 82Mhz(max). The different peripherals such as SPI, UART, TIMERs, ADCs, DACs, etc are connected to either APB1/APB2 buses. And the AHB2(168Mhz max) is connected to Camera and USB OTG interfaces, AHB3 is connected to External memory controller.


## Working Principle ##
Assume that the automobile is the microcontroller(STM32F407VG). If the button is pressed , the first led (red) will turn on, Clicking again the wiper will starts , and the second led (blue) will turn on for a desired rate. If the button is pressed again , the third led (green) will turn on, and the wiper's speed will be increased in comparison to the previous one. The fourth press will turn on the fourth led (orange) , and the wiper speed will be increased in accordance with the previous one. The microcontroller (vehicle) is turned off after the fifth click of the button.
 ## Exploring STM32F407 Discovery Board ##
 ![image](https://user-images.githubusercontent.com/86312170/168392826-07b6d456-993b-41c2-a103-0fed9ffa51aa.png)
gives practically all the fundamental data expected to begin with STM32F407 Discovery Board and furthermore advancement of driver code.

* Hardware Used : STM32F4 DISCOVERY kit, for more information visit: STM32F4 DISCOVERY
* Software Tool : STM32cubeIDE, for more information visit: STM32CubeIDE
* For installation of STM32CubeIDE refer Youtube
* Note : As this microcontroller has many advanced features and the main aim of this project is to get all basic insights, during the driver development only the required functionalities are added and other advanced functionality is not added. I may update the driver and other functionality in the future. Please find the STM32F4 Discovery User Manual,STM32F4xxx Reference Manual (RM0090) and other related documents inside a folder called Documents. I will be referring to these documents for information such as block diagrams, register details ect.

# 4W's & 1H # 
## What ##
The operational speed of a vehicle wiper is controlled by a wiper speed control mechanism based on rain conditions. To generate, the control system incorporates a rain sensor (30) that detects rain conditions. The amplitude of an analogue signal depends on the detected rain conditions.
## Why ##
To clean the windscreen clean enough to give adequate view at all times from the front and rear windshields of the car.Wiper cleans the windshield by removing oil, dust, moisture, and grime that have become attached to the glass.
## Who ##
 It is extremely important for drivers of any type of vehicle that require clear road visibility in the event of dust, snow, or rain.
## When ##
When the weather is terrible, such as snow, dust, or rain and so the windshield wipers remove rain and snow from the windshield, while the headlights improve visibility at night.
## How ##
It is implemented using the STM32 microcontroller and once when the rain droplets fall on the windshield of the vehicle.
# Output Images #
1. user button and hold it for two seconds
   ![image](https://user-images.githubusercontent.com/86312170/168393014-5233cde9-df6a-41ad-8245-27e4177c3f28.png)
2. Wiper Speed low 
![image](https://user-images.githubusercontent.com/86312170/168393095-5b46ef6a-adfc-4f16-9f5c-d16167461c06.png)
3. Wiper speed medium 

![image](https://user-images.githubusercontent.com/86312170/168393197-e0278783-f1b3-41c9-b175-e2a6197840c9.png)

4. Wiper speed high
![image](https://user-images.githubusercontent.com/86312170/168393258-5b62434b-d63f-487c-ab1d-51d628d1415a.png)

5. user button is pressed and held for 2 seconds, the red LED is off
![image](https://user-images.githubusercontent.com/86312170/168393306-55a1987b-9ff6-4ebf-aa93-b45de299ad6a.png)


# Swot Analysis #
## Strengths ##
* Hands-Free Calling.
* Automatically detects rain and wipes the windows by moving the wiper.
* Improve safety by decreasing driver distraction.
* Low Budget.
## Weakness ##
* The rain sensor-based system functions when water falls on the sensor directly.
* Week Focus on Process Innovations.
* Structural Inertia.
## Opportunities ##
* Safety.
* Hands-free calling.
* Emerging New Markets.
## Threats ##
* Low Bargaining Power Buyers.
* Ethical Pressure.
* Once the board repaired cannot be replaced quickly.

# High Level Requirements #
ID	 |  Description	                                                |     Status
-----|--------------------------------------------------------------|-------------------------
HLR-1|	Turn on the Ignition	                                      |   Implemented
HLR-2|	Activating wiper system	                                    |   Implemented
HLR-3|	Controlling the speed of the wiper based on frequency levels|	  Implemented
HLR-4|	Deactivating wiper system	                                  |   Implemented
HLR-5|	Turn off the Ignition	                                      |   Implemented

# Low level Requirements # 

ID	 |  Description	                                                                       |  Status
-----|-------------------------------------------------------------------------------------|--------------------------------------------------------
LLR-1|	Turn on the Microcontroller	                                                       | Implemented
LLR-2|	Press push button for 2secs – RED LED ON	                                         | Implemented
LLR-3|	Press push button for first time - BLUE, GREEN,ORANGE LED’s glow with 1Hz frequency|	Implemented
LLR-4|	Press push button for second time - BLUE,GREEN,ORANGE LED’s glow with 4Hz frequency|	Implemented
LLR-5|	Press push button for third time - BLUE,GREEN,ORANGE LED,s glow with 8Hz frequency |	Implemented
LLR-6|	Press push button for fourth time – ORANGE,GREEN,BLUE LED,s stops glowing	         | Implemented
LLR-7|	Press push button for 2secs – RED LED OFF	                                         | Implemented








