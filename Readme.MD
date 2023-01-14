# robotron EC1834 Mainboard Schema

Der Robotron EC1834 ist ein 8086 basierter PC.

Hier ist die digitale Version des Schaltplans von 1988, inkl. Platinen-Layout.
Die Platine wurde aktuell noch nicht geroutet, da dies beträchtlicher Zeitaufwand ist.

Falls sich das jemand antun möchte, halte ich ihn nicht davon ab... ;-)

https://www.robotrontechnik.de/index.htm?/html/computer/ec1834.htm


## Anschlüsse

### Pin Header / Bus Connector

* X1.1-8 ISA Slots
* X2 Power 12P,12N,5N,GND
* X3 Power 5P, GND
* X4 Speaker
* X5 Power On LED
* X6 Reset
* X7 Keyboard


### Prüfstecker (PSx)

PS1 5x 8288 (In/Out) 
* 1=D4p19   S0 (Output)
* 2=D4p3    S1 (Output)
* 3=D4p18   S2 (Output)
* 4=D5p11   /ROMADRSEL (8xAND Input, Pull-Up)
* 5=frei

PS2 3x 8284 (Input) 
* 1=D43p1   CSYN (Input, Pull-Down)
* 2=D43p13  F/C (Input, Pull-Down)
* 3=D4314   EFI (Input, Offen)

PS3 9x 8253 (In/Out)
* 1=D60p10      /MEMW (FF Input vom Bus)
* 2=D88p4       /MEMW - WE (FF Output D60)
* 3=D72p1       /RAS1 (AND, Input, Pull-Up)
* 4=D72p4       /RAS0 (AND, Input, Pull-Up)
* 5=D72p9       /CASL (AND, Input, Pull-Up)
* 6=D72p13      /CASH (AND, Input, Pull-Up)
* 7=D48-D49p26  /INTA (PIC, Output)
* 8=frei
* 9=frei

PS4 3x D68  (Input)
* 1=D69p9       /MEMR (AND Input, Pull-Up)
* 2=D65p5       /DACK0BRD (Binary decoder A0-A2, Input E2, Pull-Down)
* 3=D85+86p15   ADRSEL (3s Q2 Data Selector, Input S, Pull-Down)

PS5 28x Edge-RAM (Output)
*  1=D109p2  MD1    Data
*  2=D108p2  MD2    Data
*  3=D110p2  MD0    Data
*  4=D79p2   MD10   Data
*  5=D107p2  MD3    Data
*  6=D104p2  MD6    Data
*  7=D78p2   MD11   Data
*  8=D106p2  MD4    Data
*  9=D103p2  MD7    Data
* 10=D113p5  MDPEE  Parity Even Input
* 11=D77p2   MD12   Data
* 12=D105p2  MD5    Data
* 13=D76p2   MD13   Data
* 14=D91p14  MDPOA  Parity Odd Output
* 15=D74p2   MD15   Data
* 16=D86p9   A5     Address
* 17=D86p12  A7     Address
* 18=D75p2   MD14   Data
* 19=D85p12  A0     Address
* 20=D85p9   A3     Address
* 21=D86p4   A4     Address
* 22=D86p7   A6     Address
* 23=D85p7   A1     Address
* 24=D85p4   A2     Address
* 25=D117p14 MDPEA  Parity Even Output
* 26=D114p5  MDPOE  Parity Odd Input
* 27=D80p2   MD9    Data
* 28=D81p2   MD8    Data

## R-Netzwerke

R9  4x 30R serie (8288)  
R10 9mx 4k7 bus (D27)  
R11 5x 1kR bus (verteilt)  
R12 9x 4k7 bus (verteilt)  
R14 4x 30R serie (D86) 
R15 4x 30R serie (D85) 
R16 4x 30R serie (D72)  
R23 9x 4k7 bus (DIP-EMR)  
R40 8x 4k7 bus (ROM D115)  
R41 8x 4k7 bus (ROM D100)  
R52 8x 3k9 bus (verteilt)  
