# Networked IoT Gateway

 

## Project Overview

This project transforms an ESP32 microcontroller into a standalone web server. Utilizing the MicroPython `usocket` library, the device binds to Port 80 and serves an interactive HTML dashboard. This allows any device on the local network (PC, smartphone, tablet) to remotely control physical hardware components via HTTP GET requests.

 

## Architecture

* **Back-End:** MicroPython `socket` server handling TCP/IPv4 connections.

* **Front-End:** Dynamic HTML/CSS generated via Python f-strings.

* **Control Flow:** Web Browser -> `GET /?relay=on` -> ESP32 Socket -> Pin 14 High -> HTML Response.

 

## Execution

1. Flash `main.py` to the ESP32.

2. Monitor the terminal. Once connected to Wi-Fi, the ESP32 will print its IP address (e.g., `192.168.1.50`).

3. Ensure your smartphone or PC is connected to the **same Wi-Fi network**.

4. Open a web browser and type the IP address into the URL bar.

5. Use the graphical dashboard to toggle the physical hardware.