# Bluetooth Based Digital Notice Board

## Abstract

The **Bluetooth Based Digital Notice Board** is an embedded systems project that provides a smart and wireless alternative to conventional paper-based notice boards. The system allows users to send and update notices remotely using Bluetooth communication from an Android smartphone. It is designed using the **LPC2129 ARM7 Microcontroller**, which processes the received data and displays it on a scrolling **4×8×8 LED Dot Matrix Display**.

The project utilizes an **HC-05 Bluetooth module** for wireless communication through UART. To ensure secure operation, every message must be sent with a predefined passkey. The microcontroller verifies the passkey before accepting the message. If the authentication is successful, the message is stored in the **AT24C256 EEPROM**, which provides non-volatile storage so that the notice remains available even after a power failure or system restart.

The LED dot matrix display is interfaced using **74HC164 Serial-In Parallel-Out Shift Registers** for column control and a **74HC573 Octal Latch** for row selection. The system continuously reads the stored message from EEPROM and scrolls it across the display. Whenever a new authorized message is received, the current display is interrupted, the EEPROM is updated with the latest notice, and the new message begins scrolling immediately.

The project demonstrates the practical implementation of several embedded system concepts, including UART interrupt programming, Bluetooth communication, EEPROM memory interfacing, LED matrix display driving, shift register control, and real-time message processing. The firmware is developed in **Embedded C** using the **Keil µVision IDE** and programmed into the LPC2129 using **Flash Magic**.

This digital notice board eliminates the need for manually replacing printed notices, reducing paper consumption and maintenance effort while enabling instant information updates. The system is suitable for educational institutions, offices, industries, hospitals, railway stations, shopping malls, and other public locations where quick and efficient communication is required.

Overall, this project offers a reliable, low-cost, secure, and energy-efficient digital display solution that combines wireless communication with embedded technology to provide an effective real-time notice management system.
