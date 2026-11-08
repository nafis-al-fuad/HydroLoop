# HydroLoop

A futuristic real-time water treatment monitoring dashboard that visualizes a five-stage purification process with animated, sci-fi styling and MQTT updates.

<p align="center">
  <a href="https://hydroloop.pages.dev/"><strong>🌐 Visit the live site</strong></a>
  &nbsp;·&nbsp;
  <a href="https://github.com/nafis-al-fuad/HydroLoop"><strong>View on GitHub</strong></a>
</p>

## Technologies

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/MQTT-660066?style=for-the-badge&logo=mqtt&logoColor=white" alt="MQTT" />
  <img src="https://img.shields.io/badge/Cloudflare_Pages-F38020?style=for-the-badge&logo=cloudflarepages&logoColor=white" alt="Cloudflare Pages" />
</p>

<p align="center">
  <sub>Built with HTML, CSS, JavaScript, and the Paho MQTT client · Hosted on Cloudflare Pages</sub>
</p>

## Overview

HydroLoop monitors a water purification workflow and highlights its current stage:

1. Raw Intake
2. Mixing
3. Filtration
4. UV Glow
5. Storage

The single-page dashboard uses animated process cards, neon visual effects, and MQTT messages to display the active stage and system status.

## Features

- Animated boot sequence and cyberpunk-inspired dashboard
- Interactive process belt with five treatment stages
- Real-time updates via MQTT over WebSockets
- Switch between HiveMQ and EMQX brokers
- Responsive layout for desktop and mobile
- Particle background and status indicators

## Run locally

This is a static site with no build step or package installation required. Open `index.html` in a browser, or serve the project directory locally:

```bash
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## MQTT configuration

The dashboard connects to one of these public brokers over secure WebSockets:

| Broker | Host | Port | Path |
| --- | --- | ---: | --- |
| HiveMQ | `broker.hivemq.com` | `8884` | `/mqtt` |
| EMQX | `broker.emqx.io` | `8084` | `/mqtt` |

It subscribes to these topics:

- `hydroloop/bibartan26/state` — current process stage (1–5)
- `hydroloop/bibartan26/status` — system status text

To use different brokers or topics, update the `CONFIG` object in `index.html`.

## Project files

```text
HydroLoop/
├── index.html   # Dashboard, styles, and client-side logic
├── LICENSE      # MIT License
└── README.md
```

## License

Released under the MIT License. See [LICENSE](LICENSE) for details.

## Links

- **Live site:** https://hydroloop.pages.dev/
- **Repository:** https://github.com/nafis-al-fuad/HydroLoop
