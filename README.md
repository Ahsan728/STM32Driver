# Mastering Microcontroller and Embedded Driver Development 

## Development Board Used : STM32F4 Discovery Board
## IDE Used : STM32CubeIDE Eclipse based IDE
### SWO Pin (Serial Wire Output)

![image](https://github.com/user-attachments/assets/f9330123-ba44-405d-a831-2caee9faae5e)
![image](https://github.com/user-attachments/assets/3f23f0c2-0617-489d-a55f-fb61e5cdd81e)

SWD is the serial wire debug available in the microcontroller. 
- SWDIO (Bidirectional data line)
- SWCLK (Clock driven by the host)
JTAG (Joint Test Action Group) is also another kind of debugging method.
![image](https://github.com/user-attachments/assets/8f748d3c-21aa-4943-8ea7-cee5873b92f4)

# STM32 Clocks
- HSI Oscilator Clock
- HSE Oscilator Clock
- Main PLL clock

Secondary Clock Sources :
- 32KHz LSI(Low Speed Internal) -> runs watchdog, RTC, STANDby mode
- 32.768 KHz LSE (Low Speed External) -> Optionally drives RTC clock

Clock Sources:
1. Crystal Oscilator (External to the mcu) (HSE)
2. RC Oscilator (Internal to the mcu) (HSI)
3. The PLL (Phase Locked Loop) (Internal to the mcu)

**Summary of HSE** : 
HSE can be provided to the mcu via a crystal or external source (from other ckt or from another mcu)

- On the STM32-Discover board, HSE is 8MHz provided by the onboard crystal.
- On Nucleo board, HSE is of 8MHz pulled from STlink ckt.

HSI is the default clock source for the mcu, We need to enable HSE and PLL for using purpose.

**MC0** (Master Clock) is the microcontroller clock output signal.

8 channel low cost logic analyzer (https://sigrok.org/wiki/Downloads)

