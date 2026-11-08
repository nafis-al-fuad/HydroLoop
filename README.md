# HydroLoop

HydroLoop is a futuristic real-time water treatment monitoring dashboard that visualizes the purification process in a sleek, sci-fi interface. It connects to MQTT brokers, updates the active treatment stage, and presents process status information for an automated water filtration system.

## Overview

This project simulates and monitors a five-stage water purification workflow:

1. Raw Intake
2. Mixing
3. Filtration
4. UV Glow
5. Storage

The UI is built as a single-page HTML dashboard with animated transitions, neon visuals, and real-time broker communication.

## Features

- Animated “boot” sequence and cyberpunk dashboard styling
- Interactive process belt showing each purification step
- MQTT support for real-time state and status updates
- Broker switching between HiveMQ and EMQX
- Responsive design for desktop and mobile
- Particle background effects and visual status indicators

## Tech Stack

- HTML
- CSS
- JavaScript
- Paho MQTT JavaScript client
- Particle.js
- Font Awesome and Google Fonts

## Project Structure

```text
HydroLoop/
├── index.html
├── LICENSE
└── README.md
```

## How to Run

Because this project is a static web app, you can run it by opening the file directly in a browser or serving it locally.

### Option 1: Open directly

Open `index.html` in a browser.

### Option 2: Serve locally

From the project folder, run:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## MQTT Configuration

The app is configured to connect to these broker endpoints:

- HiveMQ: `broker.hivemq.com` on port `8884`
- EMQX: `broker.emqx.io` on port `8084`

It listens to the following MQTT topics:

- `hydroloop/bibartan26/state`
- `hydroloop/bibartan26/status`

These topics are used to update the displayed purification step and system status.

## Customization

You can edit the main logic in `index.html` to:

- change broker settings
- update treatment step labels
- modify colors and visual themes
- adjust MQTT topics
- tune the animation behavior

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Notes

This repository is a front-end monitoring interface for a water treatment system and is intended to be paired with connected hardware or an external MQTT publisher that emits state updates.

## Author

- DaRk77NesS

## Repository

https://github.com/nafis-al-fuad/HydroLoop
