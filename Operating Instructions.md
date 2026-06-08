### Node 3 Parameter Guide – How to Use Each Setting

Here is a clear, practical explanation of every parameter in Node 3. Each line shows the function call followed by what each argument actually controls and how you can use it.

```eel
set_p_eq(3, 5, 3000, -4.3, 0.85);
```
- **Node index** (3)  
- **Filter type** (5 = High Shelf)  
- **Frequency** (Hz) – transition point  
- **Gain** (dB) – boost or cut above the frequency  
- **Q** – transition sharpness (lower = smoother slope)  

**How to use**: Adjust gain to control brightness. Negative values tame harsh highs; positive values add air. Change frequency to move the shelf.

```eel
set_p_odd(3, 1.5, 1.0, 1.0, 0.5);
```
- **Node index**  
- **Odd harmonic intensity** (base amount)  
- **Dry multiplier**  
- **Wet multiplier**  
- **Overall mix** (0.0 = off, 1.0 = full)  

**How to use**: Increase base for more clarity, presence, and bite (especially on vocals/guitars). Lower mix for subtle enhancement.

```eel
set_p_sq(3, 0.0, 1.0, 1.0, 1.0);
set_p_tri(3, 0.0, 1.0, 1.0, 1.0);
set_p_saw(3, 0.0, 1.0, 1.0, 1.0);
set_p_fold(3, 0.0, 1.0, 1.0, 1.0);
```
Same structure as `odd`:  
- **Base** = intensity of that specific waveshape  
- **Dry / Wet multipliers + Mix** = blending control  

**How to use**: Activate individually to add square (even harmonics, aggressive), triangle (softer odd), saw (bright), or fold (complex distortion).

```eel
set_p_spread(3, 0.0, 1.0);
```
- **Node index**  
- **Spread amount** (stereo widening strength)  
- **Color** (affects which frequencies are widened more)  

**How to use**: Raise first value for wider soundstage. Higher color pushes widening toward highs.

```eel
set_p_warp(3, 0.0, 0.0, 0.0, 0.0);
```
- **Horizontal stretch**  
- **Wrap amount** (folding/wrapping intensity)  
- **Horizontal flip**  
- **Extra saw modulation**  

**How to use**: Creative tool for unusual stereo movement or aggressive reshaping. Best used subtly.

```eel
set_p_filter_mix(3, 0.0, 9000, 0.5);
```
- **Mix amount**  
- **Frequency**  
- **Resonance**  

**How to use**: Adds a variable state-variable filter. Useful for surgical tone shaping.

```eel
set_p_filter_lp(3, 14000, 0.1, 0.0);
```
- **Cutoff frequency**  
- **Slope** (steepness)  
- **Resonance**  

**How to use**: Gentle low-pass to control extreme highs and reduce harshness.

```eel
set_p_dyn(3, 0.0, 0.4, 1.0, 1.0);
```
- **Dynamic saturation amount** (base)  
- **Speed** (how fast it reacts, lower = smoother)  
- **Wet multiplier**  
- **Mix**  

**How to use**: Makes saturation responsive to signal level. Good for adding life without constant distortion.

```eel
set_p_hue(3, 0.0, 1.0, 1.0, 1.0);
```
- **Hue base** (tonal color shift)  
- **Dry / Wet / Mix**  

**How to use**: Subtle tonal tinting, often used with even harmonics.

```eel
set_p_sharp(3, -0.43, 0.8, 1.0, 1.0);
```
- **Sharpness base** (positive = sharper transients, negative = softer)  
- **Dry / Wet / Mix**  

**How to use**: Negative values reduce harsh attacks; positive values add definition.

```eel
set_p_comb(3, 0.6, 2.0, 1.0, 0.85);
```
- **Comb base** (delay / density)  
- **Dry multiplier**  
- **Wet multiplier**  
- **Mix**  

**How to use**: Creates rich phase textures and depth. Higher base = denser comb effect. Very effective for adding “air” and dimension.

```eel
set_p_even(3, 0.0, 1.0, 1.0, 1.0);
```
Similar to odd, but focuses on **even harmonics** (rounder, warmer character).

```eel
set_p_pure_shape(3, 0.0, 0.0, 0.0, 0.0);
```
Direct scaling for pure odd / square / triangle / saw shapes.

```eel
set_p_xtra_shape(3, 0.0, 0.0, 0.0, 0.0);
```
- **Exp** (exponential shaping)  
- **Log soft**  
- **Recurve**  
- **Ripple**  

**How to use**: Advanced waveshaping flavors for more complex distortion textures.

```eel
set_p_apf(3, 0.0, 3000, 1, 0.707, 4, 0.5, 1.0);
```
- **Mix**  
- **Frequency**  
- **Order**  
- **Q**  
- **Stages** (number of all-pass filters)  
- **Feedback / Feedforward**  
- **Polarity**  

**How to use**: Adds phase complexity and thickness without changing frequency balance. Increase mix and stages for richer spatial feel.

```eel
set_p_tone(3, 3000, 0, 1.0, 1.0, 1.0);
```
- **Frequency**  
- **Base amount** (tilt strength)  
- **Dry / Wet / Mix**  

**How to use**: Gentle high-frequency shelf for final tonal tilt.

```eel
set_p_ms(3, 1.0, 0.7);
```
- **Mid gain**  
- **Side gain**  

**How to use**: Control how strongly the node affects center vs sides. Lower side keeps the image focused.
