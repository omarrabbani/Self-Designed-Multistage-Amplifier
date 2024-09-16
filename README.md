# Self-Designed-Multistage-Amplifier

This project revolves around the analysis and implementation of a self constructed BJT (Bipolar Junction Transistor) that makes use of multistage amplifiers to meet the following threshold conditions.

- Power supply: +𝟏𝟎𝑽 relative to the ground;
- Quiescent current drawn from the power supply: no larger than 𝟏𝟎 𝒎𝑨;
- No-load voltage gain (at 1 𝑘𝐻𝑧): |𝑨𝒗𝒐| = 𝟓𝟎 (± 𝟏𝟎%); 
- Maximum no-load output voltage swing (at 1 𝑘𝐻𝑧): no smaller than 8 V peak to peak; 
- Loaded voltage gain (at 1 𝑘𝐻𝑧 and with 𝑅𝐿 = 1 𝑘Ω): no smaller than 𝟗𝟎% of the no-load voltage gain;
- Maximum loaded output voltage swing (at 1 𝑘𝐻𝑧 and 𝑅𝐿 = 1 𝑘Ω): no smaller than 4 V peak to peak; 
- Input resistance (at 1 𝑘𝐻𝑧): no smaller than 𝟐𝟎 𝒌𝜴; 
- Amplifier type: inverting or non-inverting; 
- Frequency response: 20 Hz to 50 kHz (−𝟑𝒅𝑩 response); 
- Type of transistors: BJT;
- Number of transistors (stages): no more than 3;
- Resistances permitted: values smaller than 𝟐𝟐𝟎 𝒌𝜴 from the E24 series;
- Capacitors permitted: 𝟎. 𝟏 𝝁𝑭, 𝟏. 𝟎 𝝁𝑭, 𝟐. 𝟐 𝝁𝑭, 𝟒. 𝟕 𝝁𝑭, 𝟏𝟎 𝝁𝑭, 𝟒𝟕 𝝁𝑭, 𝟏𝟎𝟎 𝝁𝑭, 𝟐𝟐𝟎 𝝁𝑭;

The design chosen to conform to these specifications consisted of a common collector, common emitter, and another common collector amplifier in that exact order.

![Design Project](https://github.com/user-attachments/assets/aedef1fa-0a2b-47dc-aa8d-55939b49345c)

First Stage (CC Amplifier):
In order to get a desired high input resistance Rin, a CC amplifier is extremely suitable to limit signal loss as a cause of impedance, having high input impedance as well as having a low voltage gain. Since a CC amplifier has the property of acting as a buffer, this allows for other cascaded amplifiers to output a powerful and steady signal.

Second Stage (CE Amplifier):
As a high voltage gain of 50 is specified, this automatically indicates the usage of a CE amplifier as one of its characteristics. This stage mainly provides the amplification voltage needed after a CC amplifier. Although a CE amplifier indicates low input impedance, this can be handled with a third stage as a CC amplifier.

Third Stage (CC Amplifier):
This second instance of a CC amplifier when placed after a CE amplifier creates a buffer as it possesses high input and low output impedance properties. This indicates retained voltage gain with a load in the circuit, making the no load and included load voltage gains quite consistent.
