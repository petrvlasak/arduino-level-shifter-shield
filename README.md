# Arduino Logic Level Shifter Shield

This shield is used to convert the logic 1 (HIGH) voltage at the Arduino digital pins so that logic circuits that use a different logic 1 (HIGH) voltage can be connected to it. The Shield can be used with the Arduino UNO board and any other board that has the same layout and pinout as this board. The pins are divided into three groups of eight. It is possible to choose a different voltage for each of these three groups. In the third group, only four pins are connected to the Arduino. The remaining four pins S0 - S3 are of general use and convert the IOREF voltage to the voltage set for the third group. The voltage is changed by a switch that has three options:

1. Voltage 3.3 V from Arduino
2. The voltage set by the potentiometer on the regulator varies between approximately 1.5 V - 2.8 V (the input for the regulator can be pin +5V or pin Vin)
3. External voltage - The allowed range of this voltage is 1.4V - 3.6V

## Schematic

[![Schematic](/assets/images/schematic.png)](/assets/images/schematic.png)

## Manufacturing

The PCB manufacturing files are located [here](/manufacturing/).

## Placement plan

[![Placement plan](/assets/images/placement-plan.png)](/assets/images/placement-plan.png)

## Bill of materials

| Reference | Quantity | Value | Description |
| --- | --- | --- | --- |
| C11, C14, C15, C21, C24, C25, C31, C34, C35 | 9 | 100n | Capacitor SMD 0805 |
| C12, C22, C32 | 3 | 1u | Capacitor SMD 0805 |
| C13, C23, C33 | 3 | 100u | Capacitor THT Radial D6.3mm P2.50mm |
| R11, R21, R31 | 3 | 1k | Resistor SMD 0603 |
| R12, R22, R32 | 3 | 1k | Potentiometer Bourns 3362P Vertical |
| R13, R23, R33 | 3 | 200 | Resistor SMD 0603 |
| R14, R24, R34 | 3 | 10k | Resistor SMD 0603 |
| U11, U21, U31 | 3 |  | LM317 TO-252 |
| U12, U22, U32 | 3 |  | TXS0108EPW |
| SW1, SW2, SW3 | 3 |  | OS103011MA7QP1 |
| J47, J54, J55 | 3 |  | Pin Header 1x3 2.54mm |
| J3 | 1 |  | Pin Socket 1x3 2.54mm |
| J1, J2, J51, J52 | 4 |  | Pin Socket 1x5 2.54mm |
| J56 | 1 |  | Pin Socket 1x8 2.54mm |
| J53 | 1 |  | Pin Socket 1x10 2.54mm |

Components J41, J42, J43, J44, J45 and J46 are special pin headers for Arduino shields. I found two ways to buy them:

1. From SparkFun: 1 x [Arduino Stackable Header Kit - R3](https://www.sparkfun.com/products/11417) and 2 x [Stackable Header - 3 Pin (Female, 0.1")](https://www.sparkfun.com/products/13875)
2. From Adafruit: 1 x [Shield stacking headers for Arduino (R3 Compatible)](https://www.adafruit.com/product/85)

And finally you need one Mini Jumper 1x2 2.54mm to configure the input for the regulators (+5V or Vin).
