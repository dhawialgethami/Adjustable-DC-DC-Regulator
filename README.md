# Adjustable-DC-DC-Regulator

1. Introduction
   -
adjustable DC power supply built around the LM317 three-terminal regulator. A power NPN
transistor (2N6486) acts as an external pass device to boost output current, and a smallsignal PNP transistor (2N2905) assists with limiting/protection. Input/output bypass
capacitors and a protection diode enhance stability and safety. The goal is to clarify each
functional block, derive the voltage-setting equation, and define practical limits (dropout,
current, and thermal).

2. Circuit Overview
   -
The LM317 maintains about 1.25 V between Vout and Adj. A fixed resistor from Vout to Adj
(R1) and a potentiometer from Adj to ground (R3) set the output. The external NPN pass
transistor is driven by the LM317 to deliver higher load current, while the PNP helper
transistor reduces base drive under overload to emulate current limiting. A diode prevents
the output capacitor from reverse discharging into the regulator when the input collapses.

3. Components
   -
U1 – LM317H
Q4 – 2N6486 (NPN)
Q2 – 2N2905 (PNP)
R1 (120 Ω) & R3 (5 kΩ )
C2 (10 µF), C1 (47 µF)
C3 (10 µF)
D1 – 1N4007

4. Stability and Protection
   -
Use input bypassing when the source is remote; add output capacitance for transient
performance. Bypassing the Adjust pin improves ripple rejection. Maintain a protection
diode from output to input/adjust to prevent damage during input collapse.

5.Where are they used?
-
Power supplies for embedded systems, FPGAs, CPUs
Battery-powered devices
Industrial/communications
LED drivers & motor control

6. Conclusion
   -
The LM317-based adjustable supply, augmented with a 2N6486 pass transistor and 2N2905
helper, provides a robust, simple solution for moderate output currents. With proper
headroom, heatsinking, and protection, it yields stable performance across a useful voltage
range. Designers should validate current limit thresholds and thermal margins at their
intended operating points.
10. References
• CDIL, 2N6486 – NPN Power Transistor datasheet.
• onsemi, 2N2905A – Small Signal PNP Transistor datasheet.
• Manufacturer application notes on buck/boost converters (TI, Analog Devices,STMicroelectronics).
