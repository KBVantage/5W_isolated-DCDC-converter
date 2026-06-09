# 5W Isolated DC-DC Converter

A compact 5W isolated DC-DC converter designed for portable instrumentation in factory automation applications.  
This design uses an open-loop control approach on the primary side, eliminating the need for an optocoupler while keeping the power stage simple, efficient, and compact. The design philosophy eliminates an-opto isolation feedback, which simplifies feedback and reduces component count.

---

## Overview

This project presents a 5W isolated DC-DC converter built around a TPS60402-based GaN primary-side switching stage operating at 50 kHz, with asynchronous rectification on the secondary side.  
The converter was developed for low-power industrial equipment where size, reliability, and efficiency matter. It is especially suitable for portable instruments used in factory automation, where isolated auxiliary power is often required.

At 12V input, the converter delivers up to 5V at 1A with approximately 92% efficiency.  
At 8V input, the design achieves approximately 88% efficiency.  
The open-loop architecture removes the need for optocoupler feedback, reducing cost and simplifying the design while preserving isolation benefits.

## Block Diagram

<img width="714" height="292" alt="image" src="https://github.com/user-attachments/assets/a138e0b8-864b-4b6d-ae32-5c30f47a04fd" />

---

## Key Features

- 5W isolated output power.
- 5V, 1A peak output capability.
- 50 kHz switching frequency.
- GaN-based primary-side power stage.
- Asynchronous rectification on the secondary side.
- Open-loop control, no optocoupler required.
- Designed for portable factory automation instruments.
- High efficiency: 92% at 12V input, 88% at 8V input.

---

## Topology

The converter uses an isolated flyback-style power architecture with a primary-side switching stage and a secondary-side rectification stage.  
Energy is transferred across the transformer during the switching cycle, providing galvanic isolation between input and output.  
The secondary side uses asynchronous rectification, which keeps the output stage simple and efficient for this power level.

Because the design is open loop, the output is not regulated through a feedback loop using an optocoupler.  
Instead, the design is optimized around the expected operating range, transformer ratio, switching conditions, and load profile.  
This approach is well-suited to cost-sensitive and space-constrained isolated power supplies where simplicity is a priority.

---

## Schematic Snapshot

<img width="1346" height="401" alt="image" src="https://github.com/user-attachments/assets/f97caac3-30f6-4093-aea4-bc09715399bc" />

## PCB Snapshot

<img width="1186" height="546" alt="image" src="https://github.com/user-attachments/assets/3440dc9d-fb0d-4648-9c0e-5a5d32c7d8dc" />
<img width="1110" height="448" alt="image" src="https://github.com/user-attachments/assets/758a0ab3-e676-4da5-83d0-d3b40e3a72b0" />



## Performance

| Input Voltage | Output Voltage | Output Current | Efficiency |
|---|---:|---:|---:|
| 12V | 5V | 1A peak | 92% |
| 8V | 5V | 1A peak | 88% |

These results show that the converter maintains strong performance across the intended input range while still delivering a useful isolated 5V rail for embedded and portable industrial electronics.

---

## Test Procedure

The converter was validated using bench power supplies, electronic loading, and oscilloscope measurements.  
Testing focused on startup behavior, switching waveforms, output stability, and efficiency under load.  
Measurements were taken at key operating points to confirm correct behavior at both 12V and 8V input conditions.

### Recommended test flow

1. Verify the input supply range and current limit before power-up.
2. Power the converter without load and confirm the output rises correctly.
3. Check primary-side switching waveform and transformer response on the oscilloscope.
4. Apply a light load and confirm stable operation.
5. Increase load stepwise up to 5V, 1A peak.
6. Measure input power and output power to calculate efficiency.
7. Repeat the test at 12V input and 8V input.
8. Record thermal behavior during extended operation.

### Oscilloscope captures

<img width="746" height="449" alt="image" src="https://github.com/user-attachments/assets/39301f96-6177-4bf2-a374-be5f94d83943" />

```md




```

These captures can be used to show startup, steady-state switching, output ripple, and transient performance.

---

## Design Notes

This project was developed as a practical isolated power solution for portable instrumentation in industrial environments.  
The choice of an open-loop architecture helps reduce BOM complexity and removes the need for feedback isolation components.  
The use of GaN on the primary side supports fast switching and compact power-stage implementation, while the asynchronous secondary rectifier keeps the design straightforward at 5W output power.

The result is a compact isolated converter that balances efficiency, simplicity, and manufacturability.

---

## Repository Contents

- Altium Designer source files.
- Block diagram in SVG and PDF format.
- Schematic snapshots.
- Oscilloscope captures.
- Supporting documentation and test notes.

---

## Future Improvements

- Closed-loop regulation variant.
- PCB thermal optimization.
- EMI performance characterization.
- Efficiency benchmarking across a wider input range.
- Protection feature expansion, including overcurrent and undervoltage behavior.

---

## Acknowledgments

This design was inspired by the broader class of no-opto isolated DC/DC converter architectures and reference designs used in low-power industrial applications.  
Special attention was given to compact implementation, practical testability, and suitability for portable factory automation equipment.
