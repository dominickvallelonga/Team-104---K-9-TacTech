# Team-104---K-9-TacTech
Project Description and Instructions On Running Project
----------------------------------------------------------------------------------------------------------------------------------
Below you will find all MPLAB X IDE system settings and configurations used in this project.



Pin Module
----------------------------------------------------------------------------------------------------------------------------------
* Pin Name	RA1			RA2		RA3		RA5		RB3		RB4		RB5
* Module	Pin Module		ADC		Pin Module	Pin Module	EUSART1		EUSART1		Pin Module
* Function	GPIO			ANA2		GPIO		GPIO		RX1		TX1		GPIO
* Start High	unchecked on all pins	
* Analog	no			yes		no		no		no		no		no
* Output	yes			no		no		yes		no		yes		yes
* WPU		unchecked on all pins	
* OD		unchecked on all pins	
* IOC		none on all pins	



System Module
-----------------------------------------------------------------------------------------------------------------------------------
Under "Easy Setup":
* Oscillator Select: HFINTOSC
* HF Internal Clock: 32_MHz
* Clock Divider: 1

* Watchdog Timer Enable: WDT Disabled SWDTEN is ignored

* Check "Low-voltage Programming Enable"

Under "Registers":
* Keep all default settings.



Interrupt Module
-----------------------------------------------------------------------------------------------------------------------------------
Order	Module		Interrupt	Enable
* 1	ADC		ADI		no
* 2	EUSART1		TXI		yes
* 3	EUSART1		RXI		no	
* 4	Pin Module	IOCI		yes	

Check "Single ISR per interrupt".



ADC
-----------------------------------------------------------------------------------------------------------------------------------
Under "Easy Setup":

Check "Enable ADC".
Uncheck "Enable ADC Interrupt".

* Clock source: 		FOSC/2
* Result Alignment: 		right
* Positive Reference: 		VDD
* Auto-Conversion Trigger: 	disabled

Under "Registers":
* Keep all default settings.



EUSART1
-----------------------------------------------------------------------------------------------------------------------------------
Under "Easy Setup":

Check "Enable EUSART".
Check "Enable Transmit".
Check "Enable Receive".
Check "Enable EUsART Interrupts".
Check "Redirect STDIO to USART".

* Baud Rate: 		9600 (Error: 0.040%)
* Transmission Bits: 	8-bit
* Reception Bits: 	8-bit
* Data Polarity: 	Non-Inverted

* Software Transmit Buffer Size: 8
* Software Receive Buffer Size:  8


Under "Registers":
* Keep all default settings.
