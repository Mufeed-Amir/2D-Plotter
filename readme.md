# 2D - Plotter

![Getting Started](./images/final.webp)
### This project is divided into hardware and software parts.

# Software

![Getting Started](./images/software.webp)

In software configuration, there are a lot of things from programming the Arduino to the software used and their configuration. The list of Software’s we used are

* Arduino
* Ink-Scape
* G-code Sender
* 3D-fox

Three code files :
* Check_Bluetooth.txt
* Check_Components.txt
* CNC_MainCode.txt

The first file helps you to check the working of all components before sending the main code. When all the components are working fine then send the main code and before burning any code to the Microcontroller cross-check the pin no and make sure all components are pointing to the right pin.

There is one more file to check for Bluetooth connection. In case if you want to send the g-code file wirelessly, this is optional to you but the benefit of this is, your CNC machine will be pretty handy. To access the Bluetooth configuration all you have to do is to add the Bluetooth module HC05 as shown in the circuit diagram.
```
There will be no change in the main code even after adding Bluetooth.
```

## Testing
![Getting Started](./images/testing.webp)

* Go to chrome and type "online G-code sender" extension.
* Click on the first link and add the Extension to your browser.
* Now open the g-code sender extension.
* Now load the file which you have downloaded earlier.
* Go to connect and set the configuration and then add select COM port.
* After setting up the connection with Arduino click on the "send to machine" button.

After this, your CNC machine should be able to communicate and perform the function

<b>Fox-3D : </b> is an android app, you can use this app to send the g-code file right from your phone to Microcontroller wirelessly
<b>Ink-scape : </b>Till now we know how to send the g-code but we don't know how to convert any type of image or figure into g-code, so to accomplish this we useInk-scape
# Hardware

Primary Components

* Arduino UNO
* Moter Driver
* Old DVD writers
* Servo motor
* Secondary Components (these are optional ones)

Secondary Components(these are optional ones)
* Switch
* Cooling fan
* Fuse
* LED

and other components which are needed for assistance to make the structure such as wire, cardboard, PCB plate, header pins, etc.


## Design & 3D-Model
![Getting Started](./images/design.webp)

I created this 3D model using Fusion360, It has two moving parts, in either x and y-direction. Arduino and Motor driver ICs and other components are inside the BOX fitted with a cooling fan to maintain temperature. This model is a hypothetical one, so our final prototype may look a little different to you.


## Circuit Diagram

![Getting Started](./images/circuit_diagram.webp)

 There is an Arduino and somehow every other component connected to it. There are two servo motors each govern the movement of one axis such as the x-axis and y-axis. The stepper motor we are using is bi-polar so has only four terminals. Each motor driver takes 4 input pins from Arduino and gives 4 outputs pins that go to each stepper motor. The last component is the Servo motor with 180 degrees of freedom, and is basically for lifting the pen up and pen down.

 ```
 This servomotor could run on Arduino board power, so doesn’t require any motor driver
 ```
 ## Fabrication - Circuit

![Getting Started](./images/fabrication.webp)

In the above, I have shared two diagrams one for the <b>motor driver</b> and one for the <b>voltage regulator</b>. Following this, I have soldered one voltage regulator and two motor drivers on one small <b>PCB plate</b>. And maintained the necessary connection of voltage regulator with motor driver internally. As you can see the wiring part is so complex in the diagram so, we came up with a solution to put all electronic components together on the PCB board and solder them, So after by doing this, it will be a lot easier for us to change any component during its failure.

<b>Motor-driver</b> which is in Red color is one of the most important components but also has a <b>short life</b>, due to its excessive heating of motor-driver it blows up, so to solve this problem we needed to add the <b>heat sink</b> and the IC-bed system so we could replace the <b>IC (L293D)</b> without buying a new one, So it could only be possible if we make our own set of motor-drivers by soldering it on PCB using IC-bed along without electronic components.

Just because of this, 90% percent of the wiring part is done.it makes your circuit clean and free of short-circuiting problems. If you watch carefully at back there is a plus sign of soldering wire, that actually works as a heat sink and IC doesn't get heated up. If the above circuit is very depressing to you then just buy them online. And circuit connection remain same;

## Adding Arduino
![Getting Started](./images/arduino.webp)

```
IGNORE other components in this project, like dimmer, Ignition Coil, capacitor, etc. These don't serve any purpose here. That was just for experimental purpose for High Voltage Spark Cutting.
```

## Structure & Process of Assembly
![Getting Started](./images/assembly.webp)

First, we are going to take two DVD writers and open them and then we extracted the main component that is lens pick-up assembly. This lens pickup assembly is inbuilt with one brushless motor and one stepper motor, so we don’t need a brushless motor, so remove it, and then it looks like in the 3rd slide-in diagram. Then we will put each on X and Y plane with structural support, Now we have four-wire from each stepper motor, all four wires are connected with plotter hardware inside the interior and then the wiring is done successfully.

## Result
![Getting Started](./images/result.webp)


Feel free to ask any question : mufeed.amir.17290@gmail.com / mmamir22@iitk.ac.in