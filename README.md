# ECircuits Instructions

This readme will tell you how to play ECircuits and what the heck the custom chips do ;)

# Camera Controls

WASD to move camera<br>
Scroll Wheel to zoom

# Clickmodes

Clickmodes are what tell the game what you want to do when you click a chip, pin, or something else. You can change the clickmode by clicking the large button at the bottom of the screen.

# Clickmode Controls

Click and drag a chip while in the Move clickmode to move it.<br>
Click on an output pin while in the Wire clickmode to begin a wire.<br>
Right-click in Active Wire to cancel creating the wire.<br>
Click on an input pin while in Active Wire to finish the wire.<br>
Click on the output pin of the SWITCH chip while in the Switch clickmode to toggle power.<br>
Click on the output pin of the DATA CONSTANT chip while in the Data Editor clickmode to edit data. (More on data later.)<br>
Click on any pin with wires connected to it while in the Cut clickmode to remove all wires connected to that pin.<br>
Click on any chip while in the Delete clickmode to delete the chip and cut all connected wires.<br>

# Data

Data is a type of wire/pin that allows text to be transferred. While not realistic, this prevents players from getting overwhelmed with the burdens of learning binary. It also prevents me from getting overwhelmed with the burdens of coding all the binary stuff.<br>
You can tell the difference between Data and normal wires/pins by the colors: Regular pins are black, regular wires are gray, Data pins are blue, and Data wires are pink.<br>
If you click on the output pin of the DATA CONSTANT chip while in the Data Editor clickmode, a menu will pop up that allows you to type the data into a text box. If you then wire the DATA CONSTANT chip's output into a Data input pin, such as one in the DISPLAY chip, the data will transfer through, and you'll be able to see that beautiful data!

# Chips

### Logic Chips (1.0)
The logic chips, (AND, NOT, OR, XOR, NAND, NOR, XNOR) are foundational structures in computer science, and will not be explained in this guide. You can easily find the answers on Google for these.
### SWITCH (1.0)
The switch chip is a chip with only an output. Clicking on the output while in the Switch clickmode will toggle the output power.
### DATA CONSTANT (1.0)
This is like the SWITCH chip but for Data. Clicking on the output in the Data Editor clickmode will allow you to change the Data output.
### DISPLAY (1.0)
There are two inputs to the DISPLAY chip. The first one is power. The display will not show anything unless the power is on.<br>
The second input is the Data. Feed in Data, and if the display is powered on, it will show the Data.
### MATH (1.0)
The MATH chip allows you to perform arithmetic operations on numbers fed in through Data.<br>
The first input is the first number to add/subtract/multiply/divide. There will be an error outputted if the input is not a number or if the number is too large.<br>
The second input is the second number to add/subtract/multiply/divide. There will be an error outputted if the input is not a number or if the number is too large.<br>
The third input is the operation to perform. Valid inputs are "+", "-", "\*", and "/". If something other than one of these is provided, an error will be output.
### LED (1.1)
The LED chip simply turns on the light and the output when the input is on. No longer do you need displays just to show the output of a non-Data circuit!
### EQUALS (1.1)
The EQUALS chip compares the Data inputs and powers on the output if the data is equal.
### DATASTORE (1.1)
The DATASTORE chip stores data. It has two power inputs, (referred to as 1A and 1B) and two Data inputs. (referred to as 2A and 2B)<br>
The output pin outputs the Data stored in the chip.<br>
On the rising edge (the moment where the power goes from off to on) of input 1A, the chip will store whatever data is fed in through input 2A.<br>
On the rising edge of input 2A, the chip will store whatever data is fed in through input 2A.
### HALF/FULL ADDER (1.2)
The HALF ADDER and FULL ADDER chips can be used for binary addition.<br>
The HALF ADDER takes two 1-bit inputs (A and B) and adds them. Output A is the sum and output B is the carry.<br>
The FULL ADDER is a more complete and fully modular version of the HALF ADDER. The FULL ADDER has three inputs (A, B, and Carry) and two outputs. (Sum and Carry) The third input allows you to combine multiple FULL ADDERs to do multi-bit addition.
