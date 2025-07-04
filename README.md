# CAN-CONTROLLED-AUTOMOTIVE-INFO-DISPLAY
To design and implement an embedded automotive monitoring system that collects and displays key vehicle parameters—engine temperature, fuel level, and indicator status—using the CAN (Controller Area Network) protocol for reliable and scalable communication between nodes.

⚙️ Hardware Requirements:
1) LPC 2129
2) CAN Transceiver (MCP2551)
3) LEDS
4) LCD
5) Switches
6) DS18B20 Temperature Sensor
7) Fuel Guage
8) USB to UART Converter

💻 Software Requirements:
1) EMBEDDED C – PROGRAMMING
2) KEIL-C COMPILER
3) FLASH MAGIC
   
🔑 Key Features:
1) Real-Time Monitoring: Displays temperature and fuel level live on an LCD.
2) CAN-Based Communication: Ensures reliable data exchange between distributed nodes.
3) Interrupt-Based Control: Uses external switches to activate indicators.
4) Modular Design: Each node operates independently but communicates through the CAN bus.
5) RTC Integration: Displays current time, date, and day.  

🔁 working principle:
  The entire system works by connecting three main components or nodes:
1) Main Node (Central Controller):
   * Role: Collects data from sensors (temperature, fuel) and controls the indicator LEDs. It also displays information on an LCD screen.
   * Functions:
        * Reads the temperature from the engine using a DS18B20 temperature sensor.
        * Reads the fuel level from the fuel gauge sensor.
        * Controls the indicator LEDs based on button presses (left or right indicator).
   * Displays:
       * Engine temperature
       * Fuel level (percentage)
       * Time and date from the RTC (Real-Time Clock) on an LCD screen.
2) Indicator Node:(Indicator Control)
   * Role: Controls the indicator LEDs (left or right) based on messages received from the Main Node.
   * Functions:
       * Receives CAN messages from the Main Node.
       * Turns on the left or right indicator LED based on the received signal.
4) Fuel Node:(Fuel Gauge)
   * Role: Monitors the fuel level and sends this data to the Main Node.
   * Functions:
      * Reads the fuel sensor using the ADC (Analog-to-Digital Converter) in the LPC2129.
      * Sends the fuel percentage data to the Main Node over the CAN network.

✅ Applications:
1) Vehicle Diagnostics🚗🛠️:
   The system can be extended to monitor other critical sensors in a vehicle, such as oil pressure, tire pressure, and battery status, in addition to        temperature and fuel level.
3) Advanced Driver Assistance Systems🚗🔍:
   This system can be integrated into ADAS to provide real-time information to the driver, improving decision-making for things like route planning,
   fuel efficiency, and navigation.
5) Electric Vehicles (EVs) Monitoring⚡🚗:
   For electric vehicles (EVs), the system can be used to display battery charge status, along with vehicle temperature and energy consumption.
   
📌 Conclusion:
 
  The CAN-Controlled Automotive Info Display System effectively monitors key vehicle parameters like engine temperature and fuel level, displaying thedata in real-time on      an LCD. By using the CAN protocol for communication between modules,the system enhances vehicle diagnostics and safety,providing valuable information to the driver.

   


    
  

 
