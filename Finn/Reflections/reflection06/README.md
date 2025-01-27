# Reflection 06

## Lecture reflection

### IoTEmpower basics

#### Create and initialize new node
- Start with creating a new node folder
- Edit board if needed
- Add sensors and actuators
- Initialize code on board

#### Finding documentation
- Documentation can be found on the GIT repo, under the "doc" folder

#### Finding scripts
- Scripts can be found under the "bin" folder in the GIT repo

### System in folders

#### Which topic to be called for:
- Switch on the coffee machine?
    - myhouse/kitchen/coffee-machine/switch
- Set all the lights in living room to blue?
    - myhouse/living_room/leds1/blue
    - myhouse/living_room/leds2/blue
- Turn the main power off?
    - myhouse/main/switch

#### General rule for forming topics in IoTempower?
- Make them super general, and clear on what they are meant to do 

#### When to change something in system.conf?
- When changing the access point
- When changing WiFi
- When changing the MQTT server

There are others as well, but these are the most important

#### What role does the location of system.conf play?
- To connect the node to WiFi and MQTT

### Nodes
- What needs to/can go into node.conf?
    - Everything that can be in the other config files as well
    - node.conf overwrites system.conf, system.conf overwrites etc/iotempower.conf

### Compilation
- Deploy
    - Deploy can be done via internet, can only be done one at a time to not decrease the deploy speed
- Initialize serial
    - Initialize serial must be done via a wired Raspberry Pi connection

### Filters

- What is a common problem when we measure?
    - Too much of the same data at the same time, will flow graphs 
- How can we do graphs in node-red?
    - We use the nodes from the dashboard library
- What are filters and how do they work (in Node-Red and IoTempower)?
    - Filters in Node-Red prevent the same value from being sent too my times
    - Filters in IoTEmpower can be set in the sensor configuration
- What is offered and what other generic filters would be nice?
    - Avergae, median, round, time_filter and more
- What is the “fluent” style?
    - The filter chaining 

## Lab reflection
We worked on the following assignments:

### 1. RFID Reader

The RFID reader was a simple exercise, we hooked it up to the Wemos D1 mini, ran the code and it could read the card UID on the MQTT topic. We then made the logic for "Acces granted" and "Access denied".

### 2. LED with PWM

We used the ESP32 minikit for this exercise, we struggled doing it on the Wemos because the PWM didn't want to work. So when we switched to the ESP32, changed the pin it did finally work.

### 3. Buzzer with PWM

This exercise was easy to do since we already used PWM with an LED, so using a buzzer was just replacing the LED with a buzzer and it worked.

###  4. Group project

The group project took some more time, I did the RFID reader with the traffic lights. I gave the flow with the components to Vincent who made the rest of the assignment.


