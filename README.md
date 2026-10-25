# SYNTH777-HALFLIFE


## Description

SYNTH-777 is a DIY cyberpunk-themed synthesizer made for the Hack Club Half Life week 3. It features 8 rotary encoders, 4 potentiometers, 4 buttons, 4 sliders, and a 4.3-inch touchscreen. It also comes with 42 capacitive pads to represent piano keys, spanning two octaves. As for output, it uses a 3.5mm audio jack. It powers through USB-C, and steps the power from the input voltage to 5V. This 5V is then separated into 3.3V, 2.5V, 1.8V, 1.1V, and VDDA (3.3V). As for internal processing, the brain is an ESP32-P4, connected to two MPR121QR2s to control all 24 keys. The board is designed to be printed on a 6-Layer PCB.


## Process

The process was a generic PCB process. I started by choosing a microcontroller with a lot of power and a vast array of GPIOs. I decided to use the ESP32-P4 because of its power. I chose all the encoders and potentiometers from Alpine, as they keep a consistent footprint. All the other parts were generically sourced from various verified manufacturers on LCSC. After wiring everything to its nets, the Schema was converted to a PCB. Here, the longest amount of time was spent. The project began in EasyEDA STD, and after placing all the components, I used the autorouter, as there were around 600 routes to draw and little time. The router failed on around 200 connections. After playing with the STD router, I migrated the project to Pro, as it came with a much better Autorouter. It still failed. After this, I changed all the resistors and capacitors from through-hole to SMD 1206. The through-hole components were too congested, and the SMD components allowed for easier vias. After running the router, I had to manually route around 40 connections.


## Images

<img width="881" height="675" alt="image" src="https://github.com/user-attachments/assets/0877cb52-df83-42bb-b19d-7d9bee4274ef" />

<img width="1360" height="910" alt="image" src="https://github.com/user-attachments/assets/ba62977f-8ff7-46c9-b640-6b3939e0294d" />
