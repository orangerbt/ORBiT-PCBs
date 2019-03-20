# Serial Addressable Thermometer
## Plan 1
- This version use a sub circuit to act like a enable for all the AD.
- Disadventage: the analog circuit migth cause timming damage
## Plan 2
- Use arduino compatible micro controller and use UART as communicaiton bus
- Adventage: easy for later update, easy for new member to learn
- Disadventage: limited by the arduino IDE(Cem unhappy).
## Plan 3
- Use PIC micro controller with AD, use I2C as communication
- Adventage: faster, build in assembly
- Disadventage: Hard to upgrade
## Plan 4
- Use CAN bus compatible micro controller and use CAN as communication protocal
- Adventage: CAN bus adventage, universal bus for all rocket
- Disadventage: Hard to learn and upgrade