# GaN-RF-amplifier-

# High-Power RF Amplifier for Ultracold Atom Experiments
![WhatsApp Image 2024-01-09 at 12 41 25_53eed6b5](https://github.com/StrontiumGroup/GaN-RF-amplifier-/assets/123593581/5740001a-0fde-4368-9342-6ef3125796fa)

![RfAmp_draft_13jul](https://github.com/StrontiumGroup/GaN-RF-amplifier-/assets/123593581/e7e4d185-c07e-4d4c-a956-eb8f96a12616)

This project presents the design and characterization of a high-power RF amplifier optimized for driving acousto-optic (AO) and electro-optic (EO) modulators used in ultracold atom experiments. The amplifier delivers an output power of 36.5 dBm over a frequency range of 20 MHz to 1000 MHz with a total gain of 40 dB.

## Table of Contents

- [Introduction](#introduction)
- [Design](#design)
  - [Switching Power Regulation Unit](#switching-power-regulation-unit)
  - [RF Input Signal Conditioning Stage](#rf-input-signal-conditioning-stage)
  - [RF Attenuator Stage](#rf-attenuator-stage)
  - [RF Amplification Stage](#rf-amplification-stage)
  - [Power Sequencing System](#power-sequencing-system)
  - [Thermal Management](#thermal-management)
- [Characterization](#characterization)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

This RF amplifier is designed to drive AO/EO modulators that control and modulate the frequency, amplitude, and phase of laser beams in ultracold atom experiments. It is optimized for high power efficiency (>35%) and long-term RF power stability (0.01 dBm).

## Design
Design schematics are in RF_PowerAmp_V12.pdf and gerbers and other design files are in RF_PowerAmp_V12.zip
![Screenshot 2024-05-20 140654](https://github.com/StrontiumGroup/GaN-RF-amplifier-/assets/123593581/c03c8cfe-6a49-459f-a3a2-685408cc598b)

### Switching Power Regulation Unit

The power regulation unit converts a single positive input supply voltage (21.5 to 32 V) into multiple voltages required by the RF stages. It uses a dual channel step-down regulator (LT8653S) to deliver +20 V and +8 V with >90% efficiency.

### RF Input Signal Conditioning Stage

This stage includes an absorptive RF switch and a low-noise pre-amplifier. It supports two RF input signals and selects between them using a dual-channel RF switch (HSWA2-30DR+).

### RF Attenuator Stage

The pre-amplified RF input is controlled by a voltage-controlled RF attenuator (VVA, Mini-Circuits RVA-3000R+). This stage allows for analog input voltage control and enables power stabilization using a PID loop.

### RF Amplification Stage

The amplification stage includes a pre-amplifier (Mini-Circuits LHA-13HLN+) and a high-power RF amplifier (Macom NPA1006), achieving a total gain of 37 dB and an output power of 36.5 dBm.

### Power Sequencing System

The power sequencing system ensures the negative gate voltage is applied before the positive drain voltage to protect the NPA1006 chip from damage.

### Thermal Management

The amplifier dissipates 6 W at maximum output power. It uses a 4-layer PCB design and an RF shielding case for passive air cooling. Additionally, a forced air cooling system reduces the temperature of the NPA1006 chip from 80°C to 65°C.

## Characterization

The RF amplifier has been extensively characterized for:
- Gain flatness (average gain flatness of 1.1 dB over 50-1000 MHz)
- Linearity (third-order intercept point of 52 dBm)
- Harmonic distortion (second-harmonic component at ≈ 20 dBc for maximum output power)
- Phase noise (maximum of 15 dBc/Hz increase for 36.5 dBm output power)
- Long-term power stability (standard deviation of 0.01 dBm over 30 minutes)


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For questions or support, please contact:

- **Email:** e.w.baaij@uva.nl
- p.thekkeppatt@outlook.com
- t.vanroon@uva.nl

## Reference

- Premjith Thekkeppatt, Edwin Baaij, Tijs van Roon, Klaasjan van Druten, Florian Schreck, _High-power RF amplifier for ultracold atom experiments_, ![arXiv:2506.18137 (2025)](https://arxiv.org/abs/2506.18137).
