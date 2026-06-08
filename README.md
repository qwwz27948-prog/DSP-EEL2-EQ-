### Quantum 6
A multi-stage parallel audio processing chain implemented in EEL2 for the JamesDSP real-time programmable engine.
The architecture integrates parametric equalization, dynamic range smoothing, non-linear harmonic generation, and Mid/Side domain processing using a parallel routing topology.
#### Technical Features
 * **4-Node Parallel Topology:** Features four independent processing nodes with discrete Mid/Side signal routing and matrix attenuation coefficients per node.
 * **Filtering & Phase Networks:** Implements standard Biquad EQ structures, configurable multi-stage allpass networks (supporting up to 32 stages), and first-order low-pass/high-pass tone-shaping filters.
 * **Non-Linear Waveshaping:** Contains dedicated blocks for odd/even harmonic synthesis, trigonometric and hyperbolic soft clipping, and wavefolding algorithms.
 * **Stereo Field Modification:** Includes warp and spread modules utilizing time-domain smoothing and fixed phase displacement networks.
 * **Dynamic Signal Smoothing:** Integrates an envelope-following attenuation module with configurable time-constant rate coefficients.
 * **Conditional Bypass Optimization:** Utilizes control-rate pre-calculation to evaluate state flags, allowing the engine to bypass inactive processing blocks and reduce per-sample execution overhead.
