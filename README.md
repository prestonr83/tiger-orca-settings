# Orca filament settings viewer

A single static page that shows the OrcaSlicer filament settings stored on a Tiger Studio product.
The Tiger Canvas Spools OrcaSlicer plugin adds the page as an "Orca settings" link on the product.

The settings travel inside the link, after the `#`:

```
https://prestonr83.github.io/tiger-orca-settings/#<base64url(zlib(JSON))>
```

Browsers never send the part after `#` to the server, so the page holds no data and the settings
never reach GitHub. They are decoded and shown only on the device that opens the link.

Payload:

```json
{"v": 1, "name": "ELEGOO PLA Neon Green", "color": "#39FF14", "base": "Elegoo PLA @ECC2",
 "settings": {"filament_flow_ratio": "0.95"},
 "tiger": {"filament_diameter": "1.75", "nozzle_temperature_range_low": "190"},
 "updated": 1794163085954}
```
