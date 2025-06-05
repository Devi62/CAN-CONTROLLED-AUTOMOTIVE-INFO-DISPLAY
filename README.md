# CAN-CONTROLLED-AUTOMOTIVE-INFO-DISPLAY
To design and implement an embedded automotive monitoring system that collects and displays key vehicle parameters—engine temperature, fuel level, and indicator status—using the CAN (Controller Area Network) protocol for reliable and scalable communication between nodes.

HARDWRAE REQUIREMENTS:
1) LPC 2129
2) CAN Transceiver (MCP2551)
3) LEDS
4) LCD
5) Switches
6) DS18B20 Temperature Sensor
7) Fuel Guage
8) USB to UART Converter

SOFTWARE REQUIREMENTS:
1) EMBEDDED C – PROGRAMMING
2) KEIL-C COMPILER
3) FLASH MAGIC

Key Features:
1) Real-Time Monitoring: Displays temperature and fuel level live on an LCD.
2) CAN-Based Communication: Ensures reliable data exchange between distributed nodes.
3) Interrupt-Based Control: Uses external switches to activate indicators.
4) Modular Design: Each node operates independently but communicates through the CAN bus.
5) RTC Integration: Displays current time, date, and day for added functionality.

Functionality Breakdown:
1. Main Node:
    * Reads engine temperature using DS18B20 sensor
    * Retrieves RTC (Real-Time Clock) data
    * Displays temperature, time, date, and day on LCD
    * Receives fuel data from Fuel Node and displays fuel percentage
    * Detects switch press (interrupt) and sends indicator signal to Indicator Node
    * Displays indicator status on LCD based on feedback
2. Fuel Node:
    * Continuously reads analog signal from fuel gauge sensor
    * Converts signal using on-chip ADC
    * Sends fuel percentage data to Main Node via CAN
3. Indicator Node:
   * Listens for CAN messages from Main Node
   * Turns ON/OFF LEDs representing left/right indicators
   * Helps visualize vehicle signaling behavior



