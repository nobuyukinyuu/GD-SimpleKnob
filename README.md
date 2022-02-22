
# GD-SimpleKnob ![icon_knob](https://user-images.githubusercontent.com/1023003/155073112-adb430f5-19db-45eb-a6b6-881f301a9859.svg)
SimpleKnob is a UI knob control for Godot 3.x intended to be a drop-in replacement for standard HSlider controls.  Themes and overrides created for HSlider should "just work".  Includes customizable grabber pointing orientation (inwards/outwards), knob thickness (Values < 100% create hollow or arc knobs), notch (arc) width, decimal padding, and title/value positioning.

![screenshot](https://user-images.githubusercontent.com/1023003/155067485-5918a942-3154-4292-93f7-0935c77fbcbc.gif)

# Usage
Drag Knob.tscn into your scene.  Alternatively, you can try adding one from the New Node dialog as "Knob".  The latter *should* generate a new object if the control detects it was not instanced from a scene.

## FAQ
**Q:** How do I change the title font?
- *A:  Use a Theme to change the default font.*

**Q:**  Can I hide the value display?
- *A: The easiest way to do this is to change the value font to a New BitmapFont or similar.*

**Q:**  Adjusting the knob is way too sensitive!  How do I lower the sensitivity?
- *A: Change the travel multiplier from 1.0 (which makes it behave identically to an HSlider) to a larger value.<br>  The length of travel from `min_value` to `max_value` is proportional to the size of the control times the multiplier.*

**Q:**  The theme isn't updating!
- *A: There doesn't appear to be a trivial way for a script to update the theme automatically from the editor when it changes.  To preview the changes, flick the visibility of the control off and on.  At runtime, the configuration should be automatic.*
