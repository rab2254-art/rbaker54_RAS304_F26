
# Power Budget

## Overview

The purpose of the power budget is to determine how much electrical power my Driver Nano 2 subsystem requires.

My subsystem includes the PIC18F57Q43 Curiosity Nano, Linear Actuator A, motor driver, pressure sensor, and limit switches.

A power budget is necessary to select suitable power supplies, regulators, protection devices, connectors, and wiring.

The final component specifications have not yet been confirmed, so this page explains the calculation method and identifies the measurements still needed.

## Power Requirements

Different components may operate at different voltages.

The microcontroller and sensors require a suitable low-voltage supply, while the actuator may require a separate higher-current supply.

The final supply requirements will be determined from the selected component datasheets.

## Preliminary Power Budget Table

| Component | Voltage | Current | Power |
|---|---|---|---|
| PIC18F57Q43 Curiosity Nano | To verify | To verify | Pending |
| Linear Actuator A | To verify | To verify | Pending |
| Motor Driver | To verify | To verify | Pending |
| Pressure Sensor | To verify | To verify | Pending |
| Limit-Switch Input Circuits | To verify | To verify | Pending |
| Additional Circuit Components | To verify | To verify | Pending |
| **Total** | | | **Pending** |

*Table 1. Preliminary Driver Nano 2 power budget.*

## Power Calculations

Electrical power is calculated using:

\[
P = VI
\]

Where:

- \(P\) = power in watts
- \(V\) = voltage in volts
- \(I\) = current in amperes

For a component with known voltage and current, multiply the two values to calculate its power.

### Example Calculation

For an illustrative component operating at 5 V and drawing 0.10 A:

\[
P = (5)(0.10) = 0.50\text{ W}
\]

This is an example calculation only. It is not a measured value for my subsystem.

## Total Power

Once the component specifications are confirmed, the total electrical load can be estimated by adding the power consumed by each component:

\[
P_{\text{total}} = P_1 + P_2 + \cdots + P_n
\]

The calculation must account for the actual power path so that regulator or driver losses are not counted twice.

## Actuator Power

The linear actuator is expected to be one of the larger electrical loads in the subsystem.

The following specifications must be confirmed:

- Rated operating voltage
- Normal running current
- Startup current
- Stall current
- Expected duty cycle

The power supply and motor driver must be evaluated for the relevant operating and fault conditions, not only the actuator's average power.

## Regulator Considerations

If the subsystem uses voltage regulation, the regulator must support the required output voltage and current.

Regulator efficiency or dissipation must also be considered.

For a linear regulator:

\[
P_{\text{loss}} = (V_{\text{in}} - V_{\text{out}})I
\]

This calculation estimates the regulator's power dissipation when its input and output current are approximately equal.

## Measurement Plan

After the components are selected and the circuit is assembled, I plan to verify:

1. Controller supply voltage
2. Controller current consumption
3. Sensor current consumption
4. Actuator current during movement
5. Actuator current under representative load
6. Motor-driver operating conditions
7. Total supply current

Measurements will be compared with the calculated budget.

## Design Status

| Task | Status |
|---|---|
| Identify power-consuming components | Completed |
| Identify calculation method | Completed |
| Confirm component voltage ratings | Pending |
| Confirm component current ratings | Pending |
| Calculate total power | Pending |
| Select final power supply | Pending |
| Verify measurements | Pending |

## Conclusion

The power budget provides a method for determining the electrical requirements of Driver Nano 2.

Final calculations cannot be completed until the actuator, motor driver, sensor, and power-distribution components are selected.

The completed budget will be used to verify that the electrical design can support the subsystem safely and reliably.

