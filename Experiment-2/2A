# MOSFET Amplifier Configurations (TSMC 180 nm)
Linear Integrated Circuits Laboratory

# Experiment 2

![Image](https://github.com/ullasnarahatti/Experiment-12/blob/483f8cc9e3cc4bb25205635ef02c7c52e51012f7/LIC%20FRONT.png)

This project demonstrates the design and simulation of different MOSFET amplifier configurations using TSMC 180 nm CMOS models in LTspice.
The goal is to study biasing conditions, gain behavior, and frequency response of common analog amplifier structures.

Objective

Design and analyze the following MOS amplifier circuits:

Source Degenerated Common Source Amplifier

Cascode Amplifier

Current Mirror Loaded Common Source Amplifier

The circuits are simulated to observe DC operating points, transient response, voltage gain, and frequency behavior.

# Simulation Environment
| Item            | Description   |
| --------------- | ------------- |
| Technology      | TSMC 180 nm   |
| Supply Voltage  | 1.5 V         |
| Devices Used    | NMOS and PMOS |


# MOSFET Amplifier Theory

MOSFET amplifiers are typically biased in the saturation region, where the drain current becomes largely independent of drain voltage.

#  First we take all  type of information Date

 # Equations
| Parameter         | Equation                   |
| ----------------- | -------------------------- |
| Drain Current     | ID = (1/2) μCox (W/L) Vov² |
| Transconductance  | gm = 2ID / Vov             |
| Output Resistance | ro = 1 / (λID)             |
| Voltage Gain      | Av = −gm × Rout            |

# All Parameters for NMOS and PMOS
Parameter	Value
| Parameter            | Value  |
| -------------------- | ------ |
| Technology Node      | 180 nm |
| Supply Voltage       | 1.5 V  |
| Target Drain Current | 200 µA |
| Overdrive Voltage    | 0.25 V |
| Channel Length       | 180 nm |

#  Values
| Device | Mobility           |
| ------ | ------------------ |
| NMOS   | 273.8 × 10⁻⁴ m²/Vs |
| PMOS   | 115.7 × 10⁻⁴ m²/Vs |

# Oxide Parameters
| Parameter          | Value            |
| ------------------ | ---------------- |
| Oxide Thickness    | 4.1 nm           |
| Oxide Permittivity | 3.54 × 10⁻¹¹ F/m |

Gate oxide capacitance:

Cox = εox / tox

Cox ≈ 8.63 mF/m²

# For NMOS  Process Transconductance

| Parameter  | Value     |
| ---------- | ----------|
| μnCox      | 236 µA/V² |

# Calculated Dimensions

| Device | Width (µm) | Length (µm) | W/L   |
| ------ | -----------| ------------| ------|
| NMOS   | 5          | 0.18        | 27.78 |

# For PMOS  Process Transconductance
| μpCox  | 100 µA/V² |

# Calculated Dimensions
| Device | Width (µm) | Length (µm) | W/L   |
|--------|------------|-------------|-------|
| PMOS   | 11.83      | 0.18        | 65.72 |


# Transistor Size Calculation

Using the MOSFET saturation equation:

ID = (1/2) μCox (W/L) Vov²


PMOS width is larger due to lower hole mobility.

# Circuit 2A – Source Degenerated Common Source Amplifier

For Design  a MOS amplifier that:

- Operates at 200 µA drain current

- Provides maximum symmetric output swing

DC Bias Design
| Parameter | Value   |
| --------- | ------- |
| ID        | 200 µA  |
| VTHn      | 0.36 V  |   = For NMOS
| VTHp      | −0.39 V |   = For PMOS
| VDD       | 1.5 V   |


# Drain Voltage Selection
For maximum output swing:

- VDS = VDD / 2   ,1.5/2

- VDS = 0.75 V

# Source Voltage

Chosen value:

- VS = 0.2 V

This improves bias stability.

# Output Voltage
- Vout = VDD/2+0.2 
- Vout = 1.5/2+0.2= 0.95

# Source Resistor   
 -  IDRD = VS = 0.2

- RS = IDRD / ID   0.2/200µA

- RS = 1 kΩ

# Gate Voltage

- VGS = VTH + Vov = 0.36=0.25

- VGS = 0.61 V

- VG = VGS + IDRD = 0.61+0.2

- VG = 0.81 V

# PMOS Gate Voltage

- VSG = Vov + |VTHp|

- VSG = 0.64 V

- VGp = VDD − VSG

- VGp = 0.86 V

# Saturation Verification
| Device | Condition | 
| ------ | --------- | 
| NMOS   | VDS ≥ Vov | 
| PMOS   | VSD ≥ Vov | 


Both transistors remain in saturation.

![Image](https://github.com/ullasnarahatti/Experiment-12/blob/fd089c678c43f0bb77d9d8059f67a78a3be9a1b2/DC%20op.png)

# Final Operating Point
| VS    | VDS    | Vout   | VG     | VGp    | ID     | RS   | Vov    |
| ----- | ------ | ------ | ------ | ------ | ------ | ---- | ------ |
| 0.2 V | 0.75 V | 0.95 V | 0.81 V | 0.86 V | 200 µA | 1 kΩ | 0.25 V |

# Width Optimization
Practical widths used in LTspice:

| Device | Width   |
| ------ | ------- |
| NMOS   | 15.2 µm |
| PMOS   | 37.5 µm |

Widths increas to get ID ≈ 200 µA 

# Transient Analysis
| Parameter | Value  |
| --------- | ------ |
| Frequency | 1 kHz  |
| Amplitude | 10 mV  |
| DC Bias   | 0.81 V |

LTspice input source:
- Vin = SINE(0.81 10m 1k)
  
# Input Waveform
# Output Waveform
![Image](https://github.com/ullasnarahatti/Experiment-12/blob/fea78624b45158a632674a14a3320a57fcb70bd8/Transint%20analysis.png)

# Input and Output Comparison
images/input_output.png
# Practical Gain Calculation
| Measurement | Value     |
| ----------- | --------- |
| Vin(p-p)    | 19.6 mV  |
| Vout(p-p)   | 186 mV |


Voltage gain:

- Av = Vout / Vin

- Av ≈ 9.487

- Gain in dB:

- Gain = 19.5 dB

# AC Frequency Response
| Parameter    | Value     |
| ------------ | --------- |
| Midband Gain | 19.487 dB |
| −3 dB Gain   | 16.487 dB |
| Bandwidth    | 233.8 MHz |

![Image](https://github.com/ullasnarahatti/Experiment-12/blob/8bc53798959670725f77b90df2811ab7c9ebf82a/AC%20Analysis.png)
