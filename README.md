# Rover-Card

Lovelace card for **[Rover](https://github.com/BotoVed/Rover)** — Home Assistant remote control over LoRa, when the internet is unavailable.

## What it shows

- Home name and number of connected fronts (online/total).
- Live packet flow — last 200 incoming and outgoing packets with click-to-expand details.
- Admin panel — QR onboarding for new fronts, list of registered users. Password-protected.

Device control itself is not in this card — that's what native HA cards are for. Rover Card exists to show **what's happening in the Rover radio network** that you can't see otherwise.

## Installation

### Via HACS (recommended)
1. HACS → Frontend → ⋮ → Custom repositories.
2. Add `https://github.com/BotoVed/Rover-Card` as **Lovelace** type.
3. Install **Rover Card**.
4. Reload the Lovelace page.

### Manual
1. Download `rover-card.js` from the [latest release](https://github.com/BotoVed/Rover-Card/releases).
2. Drop it into `<HA_config>/www/community/rover-card/`.
3. Add to Lovelace resources:
   ```yaml
   resources:
     - url: /hacsfiles/rover-card/rover-card.js
       type: module
   ```
4. Reload the Lovelace page.

## Usage

Add to your dashboard:
```yaml
type: custom:rover-card
```

Optional parameters:
```yaml
type: custom:rover-card
title: Rover Status
max_packets: 200
show_admin: true
```

## Build from source

```bash
npm install
npm run build
# → dist/rover-card.js
```

## Documentation

Common documents live in the main Rover repository:
- **[SPEC.md](https://github.com/BotoVed/Rover/blob/main/SPEC.md)** — protocol specification (see §10 for card details)
- **[DECISIONS.md](https://github.com/BotoVed/Rover/blob/main/DECISIONS.md)** — architectural decisions

Card-specific docs in this repository:
- **[AGENT.md](./AGENT.md)** — instructions for AI agents working on the code

## Related

- **[Rover](https://github.com/BotoVed/Rover)** — Home Assistant integration (back)
- **[Rover-App](https://github.com/BotoVed/Rover-App)** — Android application

## License

[GPL v3](https://github.com/BotoVed/Rover/blob/main/LICENSE)
