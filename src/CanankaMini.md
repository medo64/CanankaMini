### CanankaMini

#### Parts

|  # | Part                                               | RefDes  | Preferred Part Number      |
|---:|----------------------------------------------------|---------|----------------------------|
|  4 | C 100nF X7R 16V (0805)                             | C1-C4   | 478-5311-1-ND              |
|  1 | C 330nF X7R 16V (0805)                             | C5      | 732-7669-1-ND              |
|  3 | C 10uF X5R 16V (0805)                              | C6-C8   | 1276-1096-1-ND             |
|  1 | D Schottky 30V 800mA [CUS08F30,H3F] (SOD323)       | D1      | CUS08F30H3FCT-ND           |
|  4 | DS LED (0805)                                      | DS1-DS4 | 475-1415-1-ND              |
|  1 | J USB A, plug, horizontal                          | J1      | WM3983CT-ND                |
|  1 | J MC 1,5/ 4-G-3,81                                 | J2      | ED2810-ND                  |
|  1 | L Ferrite 40Ohm (0805)                             | L1      | 445-2201-1-ND              |
|  2 | Q MOSFET-P 20V 4.2A ±8Vgs [DMG2305UX-13] (SOT23-3) | Q1-Q2   | DMG2305UX-13DICT-ND        |
|  1 | R 118 0.125W (0805)                                | R1      | P118CCT-ND                 |
|  5 | R 1K 0.125W (0805)                                 | R2-R6   | RMCF0805FT1K00CT-ND        |
|  1 | R 75K 0.125W (0805)                                | R7      | RMCF0805FT75K0CT-ND        |
|  1 | U MCP2221A (TSSOP-14)                              | U1      | MCP2221A-I/ST-ND           |
|  1 | U PIC18F25K80 (SSOP-28)                            | U2      | PIC18F25K80-I/SS-ND        |
|  1 | U MCP2561 (SOIC-8)                                 | U3      | MCP2561-E/SN-ND            |
|  1 | U LoadSwitch Adjustable [AP22652W6-7] (SOT23-6)    | U4      | 31-AP22652W6-7CT-ND        |
|  1 | P MC 1,5/ 4-ST-3,81                                | P2      | ED2877-ND                  |

1/2" heat-shrink tubing, 41mm


WARNING: This is a non-isolated board - beware of ground loops and all the fun
that can happen with different ground potentials.


#### Specifications

| Property      | Value                      |
|---------------|----------------------------|
| PCB size      | 48.5 x 16.5 mm ~ 1.3 sqin  |
| Voltage (in)  | 5 V ±10%                   |
| Current (in)  | 500 mA (max)               |
| Voltage (out) | 5 V ±15%                   |
| Current (out) | 425 mA (min)               |

For testing purposes, it is possible to power other devices from 5V USB
connection. However, considering CAN bus is usually 12V based, this is
definitely not a recommendation.


#### UART Configuration ####

In order to configure the device, one has to use MCP2221 Utility application
(download from Microchip). In configuration, one MUST perform the following
changes:

    * GP1: 1 (CLK_OUT)

The following changes are suggested:

| Property                     | Value            |
|------------------------------|------------------|
| VID:                         | 0x04D8           |
| PID:                         | 0xE866           |
| Required Current:            | 500 mA           |
| Descriptor:                  | Cananka Mini     |
| Manufacturer:                | Medo64           |
| Enumerate with serial number | Yes              |
| GP1                          | CLK_OUT          |

All other settings should remain default.
