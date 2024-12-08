**Work-in-Progress** - [First Revision gerbers being tested](https://github.com/mwrnd/SFP_Plug_Breakout/releases/tag/v0.1-alpha).




# SFP_Plug_Breakout

Pluggable [SFP (SFF INF-8074i)](https://members.snia.org/document/dl/26184) and [SFP+ (SFF-8432)](https://members.snia.org/document/dl/25892) Module Breakout for developing SFP modules. PCB must be manufactured with a **1.0mm** thickness.

Similar Projects: [SFP-Breakout-Board](https://github.com/aewallin/SFP-Breakout-Board/tree/df46707f1ecbe9b7fed1791247dec31a45b60560), [SFP_BreakoutBoard](https://github.com/kingyoPiyo/SFP_BreakoutBoard), [SFP-Loopback-Board](https://github.com/aewallin/SFP-Loopback-Board), and [Sfp-breakout](https://osmocom.org/projects/misc-hardware/wiki/Sfp-breakout)(*osmocom.org*).




## PCB Layout

Differential pair parameters were calculated based on a **board thickness of 1.0mm**.

![SFP Plug Module Breakout PCB Layout](img/SFP_Plug_Module_Breakout_PCB_Design.png)




## Schematic

![SFP Plug Module Breakout Schematic](img/SFP_Plug_Module_Breakout_Schematic.png)




## Bill Of Materials

I have been testing with general purpose capacitors for the RX and TX DC-Blocking capacitors (C1, C2, C3, C4) but at <10Gbps bitrates. Capacitors will need to be sized smaller, 0402 or even 0201, and more effort would need to go into their selection for high bitrates. Look for [capacitors designed for high-frequency](https://www.digikey.ca/en/products/detail/passive-plus/0402BB104KW500/19186629).

| Designator(s)   | Part Number         | Quantity | Value   | Footprint                        | Availability                                                                                           |
| --------------- | ------------------- | -------- | ------- | -------------------------------- | ------------------------------------------------------------------------------------------------------ |
| C1, C2, C3, C4  | GRM1885C1H103JA01D  |        4 | 0.01uF  | Capacitor_SMD:C_0603_1608Metric  | [DigiKey](https://www.digikey.ca/en/products/detail/murata-electronics/GRM1885C1H103JA01D/4421555)     |
| R1, R2, R3      | RMCF0603ZT0R00      |        3 | 0-Ohm   | Resistor_SMD:R_0603_1608Metric   | [DigiKey](https://www.digikey.ca/en/products/detail/stackpole-electronics-inc/RMCF0603ZT0R00/1756908)  |
| R10, R11, R12   | RNCF0603DTE10K0     |        3 | 10k-Ohm | Resistor_SMD:R_0603_1608Metric   | [DigiKey](https://www.digikey.ca/en/products/detail/stackpole-electronics-inc/RNCF0603DTE10K0/1708145) |
| J6              | PH2-12-UA           |        1 | N/A     | Conn_02x06                       | [DigiKey](https://www.digikey.ca/en/products/detail/adam-tech/PH2-12-UA/9830397)                       |
| J2, J3, J4, J5  | CONUFL001-SMD-T     |        4 | N/A     | U.FL_w_Label:U.FL_Hirose_w_Label | [DigiKey](https://www.digikey.ca/en/products/detail/te-connectivity-linx/CONUFL001-SMD-T/7427732)      |
| U.FL-to-U.FL    | 2015698-2           |        2 | N/A     | None - Optional Part for Testing | [DigiKey](https://www.digikey.ca/en/products/detail/te-connectivity-amp-connectors/2015698-2/1249186)  |



