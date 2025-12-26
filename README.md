# Dynamic Shadows Module v0.0.3

A **pseudo-3D dynamic shadow module** for Ikemen GO using ZSS.
This module simulates real-time shadow projection based on a per-stage configurable **light source position**.

---

## How It Works

This module creates a **pseudo light object** using a helper and modifies player shadows relative to the position of the player from the light source.

### Stage Constants

```ini
[Constants]
LightPosX = 0
LightPosY = 0
LightPosZ = 0
LightDisableZOffset = 0
LightZOffset = 0
```

### Definitions

```ini
LightPosX - X Position of the Light Object. Negative values go left, Positive values go right. 0 by default if left undefined.
LightPosY - Y Position of the Light Object. Negative values go up, Positive values go down. 0 by default if left undefined.
LightPosZ - Z Position of the Light Object. Negative values go up, Positive values go down. 0 if left undefined whenever LightDisableZOffset is on, -30 if left undefined whenever LightDisableZOffset is off. This is ignored on stages without Z Axis.
LightDisableZOffset - Disables Z Offset of the Light Object. Use this for stages with Z Axis.
LightZOffset - Z Offset of the Light Object. Treat this like LightPosZ for stages without Z Axis.
```

### Debug Mode

There's a debug mode feature that's enabled by default. To access debug mode, play on training mode and press start on P2.
I suggest going on actual Debug Mode by pressing CTRL+D on your keyboard to see the Light Object move. (AllowDebugMode must be 1 in your config.ini)

### Movement Modes

There are two movement modes. Pressing start on P2 will have the P2 toggle between them.
Use the P2 Movement Keys to move the light object during X&Y/X&Z Mode.

### X & Y Mode

Accessed by pressing Start on P2 once.
Pressing Up will move the light object up and pressing Down will move the light object down.
Pressing Left will move the light object to the left and Pressing Right will move the light object to the right.

Pressing Start while in this state will put P2 in X&Z Mode.

### X & Z Mode

Accessed by pressing Start on P2 twice.
Pressing Up will move the light object away from the screen and Pressing Down will move the light object towards the screen.
Pressing Left will move the light object to the left and Pressing Right will move the light object to the right.

Pressing Start while in this state will put P2 out of Debug mode.

---
