# Optical Theremin — Touchless Analog Musical Instrument

A breadboard-built optical theremin prototype that uses changes in light intensity to control the frequency of an audio oscillator.

## Project overview

The project explores a simple contactless way to control sound. An LDR senses changes in light as a hand moves near it. The LDR is used in the timing network of an NE555 oscillator, so changes in resistance can change the oscillator frequency. The output is sent to an audio stage for listening.

## How it works

1. **Light sensing:** The LDR's resistance varies with incident light.
2. **Frequency generation:** The NE555 is configured as an astable oscillator. Its timing network determines the output frequency.
3. **Audio output:** The oscillator signal is coupled to an LM386 audio amplifier, which is intended to drive a small 8-ohm speaker.
4. **Hand control:** Moving a hand to shade the LDR changes the light level and can therefore change the generated tone.

The direction and amount of pitch change depend on the final LDR and potentiometer wiring and component values.

## Main components

| Component | Purpose |
|---|---|
| NE555 timer IC | Generates the audio-frequency oscillator signal |
| LDR | Detects changes in light intensity |
| 100 kΩ potentiometer | Adjusts the oscillator timing range |
| 1 kΩ resistor | Part of the timing network |
| 10 nF capacitors | Timing and control-pin decoupling |
| 0.1 µF capacitor | Supply decoupling |
| LM386 audio amplifier | Amplifies the audio signal |
| 10 µF capacitor | Input signal coupling |
| 100 µF capacitor | Speaker output coupling |
| 8 Ω speaker / buzzer for bench testing | Sound output |
| 9 V battery | Power source |
| Breadboard and jumper wires | Prototyping and interconnection |

## Circuit and hardware

- Add the final, checked schematic to `Circuit-Diagram/`.
- Add clear photographs of the assembled breadboard to `Hardware-Images/`.
- Add a short demonstration clip to `Working-Video/` if available.

> **Important:** The schematic should match the actual working breadboard circuit. Verify the NE555 timing network, LM386 pin connections, capacitor polarities, and common ground before reproducing the circuit. An active buzzer has an internal oscillator and is not a suitable substitute for a speaker when evaluating continuous pitch control.

## Build status

The breadboard prototype has been assembled and tested for audible output. The buzzer produced a squealing tone during testing; continuous pitch tracking against hand movement should be documented only after it has been specifically verified. The preferred final output stage is an LM386 driving an 8 Ω speaker.

## Learning outcomes

- Astable operation of the NE555 timer
- RC charging and discharging
- Light-dependent resistance and sensor interfacing
- Frequency control using a variable timing network
- AC signal coupling and audio amplification
- Breadboard prototyping and circuit troubleshooting

## Future improvements

- Verify and calibrate the LDR-to-pitch response.
- Use a small 8 Ω speaker for clearer audio evaluation.
- Optimize the oscillator's usable musical frequency range.
- Add enclosure, light shielding, and accessible sensitivity/volume controls.
- Document measured frequencies and the final circuit values.

## Safety and reproduction notes

Use a regulated 5–9 V DC supply within the ratings of the particular ICs and components. Check IC orientation and electrolytic capacitor polarity before powering the circuit. Disconnect power before changing breadboard wiring.
