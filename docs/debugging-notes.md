# Debugging Notes

## Encoder Signal Noise

Observed unstable encoder pulse edges during high RPM operation.

### Observation
- Noise appeared on quadrature lines during acceleration
- Pulse instability affected RPM measurements

### Investigation
- Inspected encoder outputs using oscilloscope
- Checked grounding and signal routing

### Resolution
- Applied signal filtering
- Improved wiring layout
- Stabilized encoder pulse capture before STM32 timer processing
