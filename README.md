# overcurrent-protection-coordination-etap

# Overcurrent Protection Coordination & Relay Setting (ETAP)

This repository documents a power-system protection study focused on **overcurrent protection coordination**
using **ETAP**. The work includes modeling a one-line diagram, defining relay/fuse settings, plotting **TCC curves**,
and validating the **sequence of operation** under fault scenarios.

ETAP Files: https://drive.google.com/drive/folders/1fOOBKLkbA9YD1UxnivVjI591JafuaPr6?usp=sharing

## Objective
- Build a one-line model and define protection zones
- Configure overcurrent protection settings (pickup, curve type, TMS/time dial)
- Evaluate coordination/selectivity using **TCC curves**
- Verify protection sequence under different fault cases and identify miscoordination risks

## Tools
- ETAP (protection coordination, TCC plotting, sequence of operation)
- Spreadsheet (setting tables, comparison)

## Protection Settings & Observations (Summary)

### Device Settings (as configured in the study)
- **Fuses (FS1, FS2)**: EI characteristic for fault protection on **Bus C**, rated **125 A** and **160 A** respectively.
- **Relays (R1, R2)**: EI characteristic to protect **Bus C**, with operation around **480 A** (slightly above the full-load current of **410 A**).
- **Relay R3 (Bus B)**: dual setting approach using **EI** and **instantaneous** element.
- **Relay R4 (Bus A)**: SI characteristic with pickup around **3010 A**, close to the full-load current reference used in the model.
- **Relay R5 (Bus A)**: SI characteristic, considering a maximum fault current of approximately **22,700 A**.

### Fault Case Behavior
- Fault scenarios **below the reactor** followed the expected protection sequence.
- For fault cases at **Load 5** and **Load 6**, some protective devices did **not operate in the expected nearest-to-fault order**, indicating potential coordination/miscoordination behavior that requires setting review.

### Protection Philosophy Notes
- **Incoming-side protection** aims to protect the transformer against upstream supply issues (e.g., overcurrent/overvoltage on the supply path).
- **Outgoing-side protection** aims to protect the transformer against downstream faults occurring on loads or distribution lines after the transformer.


![sld](https://github.com/izzudin01/overcurrent-protection-coordination-etap/blob/main/Screenshot%202026-02-12%20163322.png)

![diagram](https://github.com/izzudin01/overcurrent-protection-coordination-etap/blob/main/Screenshot%202026-02-12%20163353.png)

## Notes
This repository is for portfolio and learning documentation purposes.
