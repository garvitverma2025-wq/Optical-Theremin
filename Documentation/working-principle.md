# Working Principle

## Optical sensing

An LDR (photoresistor) changes resistance according to the light incident on its surface. In general, resistance decreases as illumination increases and increases as illumination decreases.

## Oscillator

The NE555 can be wired in astable mode. An external resistor-capacitor timing network causes its timing capacitor to charge and discharge between internal threshold levels. The output at pin 3 is a repeating waveform. The timing resistance and capacitance determine the oscillation frequency.

For a conventional 555 astable circuit:

```
f ≈ 1.44 / ((RA + 2RB) × C)
```

This expression applies to the conventional astable topology. An LDR can be incorporated into the timing network so illumination changes its effective resistance and hence the frequency. The actual response depends on the circuit topology and values.

## Audio stage

The LM386 is a low-voltage audio power amplifier. A coupling capacitor can feed the oscillator waveform into its input while blocking the steady DC component. A second coupling capacitor at the output is commonly used to connect a single-ended speaker load.

## Demonstration

Move a hand to shade the LDR and observe whether the oscillator tone changes. Record the actual response only after testing it with a suitable speaker or measurement instrument. An active buzzer may produce its own internally generated tone and is not a reliable indicator of the oscillator's pitch.
