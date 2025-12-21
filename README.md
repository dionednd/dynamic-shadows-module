# Dynamic Shadows Module v0.0.1

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
```

---
