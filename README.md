# 🛜 Smart Refrigerator Water Dispenser
Vist the WEB-APP Repo [HERE](https://github.com/loty2019/water-dispenser-web) !

Schematics, code, [Web-app](https://github.com/loty2019/water-dispenser-web) and [3D files](https://github.com/loty2019/RefrigeratorWaterDispenser/tree/RelayWaterDispenser/STL%20files) all available.

## ℹ️ Overview
This project aims to automate the refrigerator water dispenser. Originally located inside the fridge, it has been moved outside using a custom 3D-designed fountain. We first prototyped it on Arduino and then transitioned to the ESP32 platform with internet capabilities. The entire system now operates on a database hosted on Firebase.

### Purpose (Why should this exist?)

The fridge has an internal water dispensing system that is manual. You have to hold the water bottle up, then at the same time press a hard button. In this process, the refrigerator loses coldness, and you get cold. Our system, however, utilizes an external custom-designed fountain that provides cold water after just 2 seconds of water flowing with no need to hold or press anything.

## 🗂️ Features

### 1. Remote Control

Our system reads signals from a remote controller, a simple numeric keypad used to navigate menus, set parameters, and choose which water bottle to fill and how.

### 2. Display

The 1602 display with I2C protocol provides real-time information.

### 3. Motion Activation

We've integrated a motion sensor that wakes the device from deep sleep only when someone approaches for water, enhancing energy efficiency.

### 4. Web App

We chose to use Next.js, React and Tailwind CSS to develop a simple yet useful UI to keep track of the water consumption of each user.

### 5. Custom Feature

Hosting guests or following a recipe that demands an exact amount of water? Input the desired ounces, enable unlimited fill, and so on... a handy extra feature for any occasion.

### 6. Relay

To communicate with the fridge on when to open the flow, we decided to use a relay since it allows handling 120V currents with just a 3.3V board.

### 7. Internet

Everything from water consumption to settings will be stored on a Firebase real-time database.

## Settings, Error Handling, and Details

We calculated the dispenser's flow rate and programmed the ESP to adjust the dispensing time accordingly. The user can also adjust it, and everything will be stored on the Flash memory and the database.

### Error Documentation:
Error #01 = Failed to record individual water consumption.

Error #02 = Failed to push consumption to the database.

Error #03 = Failed to generate date or hour due to connection issues.

Others coming soon...

### How to Build (soldering might be required)

- Follow the schematics and picture attached below (these are for the prototype) if you are not using the I2C protocol to cominicate with the display then use a NPN transistor to turn off the screen.
  I actually used a 3 pin relay so the image below is not accurate
<img width="847" alt="" src="https://github.com/loty2019/RefrigeratorWaterDispenser/assets/125715080/e65917bb-6f01-427a-8e4f-efa38740c8e7">
[Water Dispenser.pdf](https://github.com/loty2019/RefrigeratorWaterDispenser/files/13521786/Water.Dispenser.pdf)

- 3D printable files are in STL_files folder

![fusion fauntain v2](https://github.com/loty2019/RefrigeratorWaterDispenser/assets/125715080/9ec73046-ca15-4542-b037-f5fd5d028dbc)

- Set up a database and a web app

<img width="1321" alt="Screenshot 2024-03-16 at 11 35 05 AM" src="https://github.com/loty2019/RefrigeratorWaterDispenser/assets/125715080/f05776af-bb97-45fa-b0fc-649a54ad1cb1">


- Final Product
<img height="500" alt="" src="https://github.com/loty2019/RefrigeratorWaterDispenser/assets/125715080/d4fbf3be-4637-4666-ac03-96233b9b80b8">

https://github.com/loty2019/RefrigeratorWaterDispenser/assets/125715080/05de6919-4a6a-43a9-aefa-cd7f2b6fba2c

Collaboration: Lorenzo, Jongsoo, Minh

