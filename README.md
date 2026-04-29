<img width="1536" height="1024" alt="ChatGPT Image Apr 14, 2026, 03_17_37 AM" src="https://github.com/user-attachments/assets/69fe0333-fd68-4d5b-ba84-63096b8af394" />

# Starship ASMR Simulator

**A browser-based ambient starship cockpit experience designed for relaxation, immersion, and creative production.  The simulator is not software, it's not developed.  It is an interactive painting that has been drawn with bits and keystrokes instead of paint and brushes. It is an experiment of AI-assisted "vibe coding".**




*Authored by M.B. Parks*

---

## What Is This?

This is not a game. There are no objectives, no scores, no fail states.

Starship ASMR Simulator is a single HTML file that transforms your browser into the cockpit of a deep-space vessel. It's designed to run in full screen alongside ambient audio — particularly space traffic control and starship ambience tracks — to create an immersive, calming experience that feels like sitting at the helm of a ship cruising through interstellar space.

**Recommended audio pairing:** [Space Traffic Control ASMR](https://www.youtube.com/watch?v=-q4XwtdSxDE)

[**Test the Sim Here**](https://mbparks.com/starship)

### Use Cases

- **ASMR / Ambient Relaxation** — Run it full screen with headphones. The engine hum, soft console blips, and occasional radio chatter create a deeply calming soundscape. Interact as much or as little as you want.
- **Film & Video Production** — Need a convincing cockpit display for a short film, YouTube video, or stream overlay? This provides a realistic, animated starship interface with working readouts, comms chatter, and interactive systems.
- **Streaming Background** — Use it as an animated backdrop for podcasts, lo-fi streams, or creative work sessions.
- **Worldbuilding & Creative Writing** — Writers working on science fiction can use this as an ambient writing environment that keeps them in the headspace of their story.
- **Focus / Study Aid** — The gentle hum and slow-moving starfield provide a non-distracting ambient environment for deep work.

## Quick Start

1. Download `starship-cockpit.html`
2. Open it in any modern browser (Chrome, Firefox, Edge, Safari)
3. Name your ship and select a difficulty profile
4. Click **Engage Systems**
5. Press **F** or double-click for full screen
6. Pair with your favorite space ambient audio

No server, no dependencies, no build step. It's a single self-contained HTML file.

Looking for a tricorder sim for iOS or Android? [**Click Here**](https://github.com/mbparks/SAS_Tricorder)

---

## Features

### Viewport & Starfield

- 3D forward-flying starfield with parallax depth, star color variation, nebulae with lightning, comets, tumbling asteroids, distant ships with nav lights, planets with lit-side shading
- Bioluminescent space organisms — rare glowing jellyfish-like creatures, scannable with crew reactions
- Distant supernova — 3-phase flash with deep bass rumble, every 10-25 minutes
- CRT scanline overlay, vignette, lens flare, mouse parallax, condensation drips, day/night cockpit cycle
- Starfield density variation — star count shifts over time simulating denser and sparser regions
- Red Alert mode — full cockpit emergency red lighting with CSS classes on body

### Cockpit Interface

- Top panel — 6 system status bars. Left panel — 9 toggle switches with LEDs and tooltips. Right panel — 7 live readouts
- Bottom console — HUD data, buttons, volume/throttle sliders, Engine/Map/Probe/Tractor/Warp/Red Alert controls
- Nav compass, oscilloscope, radar/lidar, mission clock (100x), crew activity log, fuel consumption graph
- Space weather radar — solar wind, radiation, magnetic fields with real shield/radiation effects
- System status grid — 8 clickable systems with detail popups
- Panel wear texture — subtle grain and scratch effects on bezel surfaces
- Custom scrollbars matching cockpit aesthetic

### HUD Overlay

Toggle the HUD button to project a translucent heads-up display onto the viewport with color-coded sections:

- Status indicator (green/amber/red), Navigation (green), Shields & Weapons (red), Engineering (yellow), Fuel (cyan)
- Throttle bar color-coded by level
- Course track with animated waypoints, ship marker, per-leg distances, and ETA
- 3D Glide slope — large canvas-rendered approach tunnel with neon green rings, flight path diamond marker, motion trail, crosshair with pitch ladder

### Audio (Web Audio API)

All audio is procedurally generated — no external files. Engine hum, air circulation, console blips, radio static, scanner pings, button clicks, warp sounds, proximity alerts, weapons sounds, tractor beam, shuttle catapult, magnetic lock clunks, Cosmo's purring.

### Communications

- 20+ procedural radio messages with reply system and follow-ups
- Hail system with multi-turn conversations (10+ contacts)
- Comms log, Captain's log input, Ship's AI terminal
- Distress signal with safety cover, SOS morse, red alert
- Signal decryption puzzle — 3-dial frequency matching with 12 lore fragments
- Unknown signal replies — "Triangulate" returns bearing/distance; "Ignore and log" archives data

### Navigation & Helm

- **Star map** — toggleable constellation/waypoint overlay with sector grid
- **Navigation planner** — 12 star systems with full data (star type, planets, hazards, faction, fuel depot, relay status), zoom/pan (0.5x–4x), fog of war that clears as you travel, live ship position on route, clickable system detail cards ("NO DATA — Survey required" for unvisited), animated hyperspace lanes with 1.4x speed bonus, nebula background, 3D depth indicators, animated route lines with per-leg fuel/time/lane estimates, territorial boundaries triggering jurisdiction comms, comm relay coverage circles, right-click custom waypoint naming, clear route button
- **Helm control** — bearing/mark/velocity inputs, yaw/pitch/roll sliders with spring-back, click-drag starfield pan, heading updates propagated to viewport
- **Warp drive** with star streaks and rising engine pitch

### Long Range Scanner (LRS)

- Animated sonar sweep line with real-time object movement, trails, and trajectory projections
- Collision course detection with warning indicators
- Click-to-select with detail sidebar (type, bearing, range, velocity)
- Right-click context menu: Scan, Hail, Set Intercept, Launch Probe, Tractor, Track
- Double-click track mode, drag-to-measure with ETA calculation
- Contact log sidebar with timestamped entries
- 700×700 canvas with enlarged fonts

### Science & Exploration

- **Object scanning** — Hover any space object and click "Scan" for a 3-second analysis with progress bar and sweep sound. Returns a data card with composition, mass, temperature, origin, and threat level.
- **Deep scan probe** — Launch a sensor probe toward a random target. 60-second transit with countdown. Returns standard, notable (22%), or exceptional findings (8% — alien artifacts, first contact evidence).
- **Signal decryption** — 3-dial frequency matching puzzle when "Unknown Signal" messages appear. 12 lore fragments about trade disputes, military movements, and ancient beacons.
- **Nebula sample collection** — Deploy a collector during nebula proximity for 30 seconds. Returns spectrographic analysis with classification, elemental composition, and emission spectrum.
- **Discovery log** — Persistent archive of all scanned objects, probe returns, decoded signals, collected samples, and triangulated signals

### Tractor Beam

- Arm via bottom console button, lock onto asteroids or bio creatures on the LRS
- Visible beam connects ship to target
- Release to cargo bay or set adrift
- Tracked in session stats and end of watch report

### Emergency Systems

- **Emergency override panel** — Reactor Scram (dims all systems for 8s), Emergency Vent (drops pressure with rushing air sound), Thruster Override (ship shakes for 5s with thruster bursts)
- **Maintenance events** — System degradation with notification and escalation timer. Ignore for 60s and it goes critical with cascading failures. 4-step diagnostic repair or 7 unique mini-game puzzles.
- **Proximity alerts** — Amber bezel flash with two-tone alarm when asteroids pass close
- **Screen flicker/interference** — Visual static on Unknown Signal radio transmissions

### Engineering — Unique Gauges Per System

Each of the 7 systems has a unique Live display and a History tab:

- Reactor Core — 3 arc gauges (Plasma/Containment/Flux) with pulse glow; 3-line history
- Coolant Loop — Vertical thermometer with bubbles + mini graph; single-line history
- Hull Integrity — Top-down ship wireframe with 28 hull plates, stress heatmap (blue to red), micro-meteorite impacts, scanning sweep, fracture lines, 7-row readout panel; single-line history
- Shield Emitters — Wide elliptical shield bubble with 4 color-coded quadrants, hexagonal grid, impact particles; 4-line history (FWD/PORT/STBD/AFT)
- Life Support — 3 vertical bars (O2/CO2/Humidity) with target zones; 3-line history
- Port/Starboard Thrusters — Tachometer dials with vibrating needles, colored zones, 5-row readout panels (Output, RPM, Temp, Vibration, Fuel Flow)

Per-system: restart, component deep-dive (8 components), bypass routing, efficiency tuning, alert thresholds, maintenance history, recommendations.

### Repair Mini-Games (7 Unique Puzzles)

Coolant (leak detection), Thruster (bolt tightening), Sensor (frequency alignment), Deflector (sequence memory), Comms (wire matching), Air Recycler (thermal management), Default (pressure balancing). Crew assistance after 2 failures.

### Weapons System

- **Tactical viewport** — full targeting display with grid overlay, center crosshair, and mouse-tracking reticle
- **Target lock** — click contacts for animated corner brackets, pulsing ring, and lock tone
- **Laser array** — adjustable intensity (10–100%), frequency (IR through Gamma), mode (Pulse/Beam), heat management with overheat cooldown, visual beam/pulse effects
- **Torpedo bay** — 8-tube rack with visual loaded/empty indicators, torpedo trails, 85% hit chance, 300-second auto-reload per tube with countdown display
- **Shield distribution** — 3×3 directional grid, click to reinforce sectors
- **Weapons log** — timestamped record of hits, misses, launches, destructions

### Shuttle Bay (LSO Experience)

Stay on the bridge as Landing Signal Officer: mission select (Recon/Salvage/Repair/SAR), random pilot assignment, 6-step pre-launch checklist, catapult launch with countdown and screen shake, deployed tracking radar, recovery approach with guide lights and approach indicator, "Call the Ball" trap timing, auto-recovery after 3 wave-offs. Salvage missions add cargo to the cargo bay.

### Cargo Module

Full cargo bay with 24-bay isometric grid, 16 pre-loaded items across 7 types (supply/equipment/biological/hazardous/classified/personal/salvage), mass distribution indicator, environment monitoring, animated forklift bot, and 4 mini-games:

- Cargo Loading — place 3 incoming containers in 60 seconds
- Contraband Scanner — X-ray inspection, flag anomalies, choose Quarantine/Jettison/Ignore
- Emergency Jettison — hull breach, jettison containers to reach target mass in 30 seconds
- Cargo Crane — mouse-controlled crane with swinging physics, grab and place salvage

### Ship Schematic

5 decks (Bridge, Deck 1-3, Hangar) with 22 rooms. Click for details, room-specific actions (bio-scan, cargo ops, security, cryo wake, shuttle bay ops). Lockable bulkheads.

### Exterior Cameras & PIP

- **4 camera feeds** (Forward, Port, Starboard, Aft) with directional star drift and occasional static on Camera 4
- **Draggable PIP window** — picture-in-picture aft camera showing stars streaming away

### Crew Manifest

- 6 crew members with roles, locations, heart rates, and status (including one in cryo)

### Fuel Management

Dual gauges, burn rate, projected range, consumption history, spectrograph, phase diagram, efficiency grading, rationing presets, eco throttle, jettison, route costs, event log.

### Power Allocation

5 systems sharing 500 reactor units with real effects. Overload >130% risks burnout.

### Ship Database

Ship specs, Star Systems, Mission Brief with interactive objectives (add/complete/delete), Crew Bios, Captain's Notes (localStorage-persisted).

### Cosmo the Ship's Cat

17 crew log events every 2-5 minutes. Occasionally appears in Rec Room with purring sound button. Cargo bay appearances.

### Narrative Systems

- The Signal — 12-phase slow-burn mystery over 30-60 minutes, never resolves
- Ship's AI Dreams — philosophical musings after 45+ minutes, 10 unique dreams
- Idle Captain Mode — AI assumes watch after 10 minutes idle, auto-manages ship, summary on return

### Environmental Events

- **Solar flare warnings** — 30-second countdown, shield-dependent radiation impact, crew screening
- **Gravitational anomalies** — 30 seconds of instrument haywire, viewport hue warp, screen shake, discovery logged
- **Bioluminescent organism encounters** — crew wonder reactions, scannable specimens
- **Distant supernova** — 3-phase visual (flash → expanding ring → fade) with bass rumble
- **Encrypted signal interceptions** — periodic with decrypt puzzle and lore fragments
- **Starfield density variation** — star count gradually shifts, simulating denser and sparser regions
- **Proximity alerts** — amber bezel flash with alarm for close asteroid passes

### End of Watch Report

24 metrics across 11 sections including Cargo Operations. Email feature opens mail client with full plain-text report.

### Configuration

Ship naming (localStorage), difficulty presets, audio mixer, custom scrollbars.

---

## Controls

| Action | Control |
|--------|---------|
| Full screen | Press F or double-click |
| Pan starfield | Click and drag |
| Scanner ping | Click starfield |
| Scan object | Hover object, click Scan |
| Hail ship | Hover ship, click Hail |
| Volume / Throttle | Bottom-right sliders |
| HUD toggle | HUD button in toggle bar |
| All screens | Toggle bar above bottom console |

Toggle Bar: Ship, Comms, Scanner, Data, Engr, Crew, Nav, Cams, Misn, Mix, PIP, AI, Fuel, Disc, Fly, Hail, Power, Watch, Wpns, Bay, Cargo, HUD

---

## Technical Details

- Single file — ~9,400 lines, ~560KB of self-contained HTML/CSS/JavaScript
- Web Audio API — all sound procedurally generated
- Canvas rendering — starfield, engineering gauges, hull wireframe, shield bubble, radar, weapons, shuttle bay, cargo grid, glide slope
- CSS-only cockpit with clamp() responsive sizing
- 60fps requestAnimationFrame rendering
- localStorage persistence for ship name, difficulty, captain's notes
- No frameworks — vanilla JavaScript throughout

Browser compatibility: Chrome 90+, Firefox 90+, Edge 90+, Safari 15+

---

## For Filmmakers
If you're using this as a prop display for film or video production:

- The cockpit adapts to any screen aspect ratio via responsive CSS
- Ship name is customizable to match your production
- All UI text uses monospace fonts for a consistent sci-fi aesthetic
- The starfield, HUD, and system readouts look convincing on camera
- Radio chatter provides natural ambient dialogue
- The oscilloscope, radar, and status grid add visual interest to cockpit shots
- Run in full screen and frame your shot around the viewport for a "looking out the window" perspective
- Use Peaceful Cruise mode to prevent disruptive maintenance alerts during takes

---

## License
This project is provided as-is for personal, creative, and educational use.

---

## Recommended Setup

1. Large monitor or TV
2. Full screen (F key)
3. Dim room lights
4. Headphones
5. Open the recommended audio in another tab
6. Peaceful Cruise for relaxation, Standard Patrol for activity

---

*Drawn with care for anyone who's ever looked up at the stars and imagined what it would be like to be out there.*

Like what you see? [Buy me a coffee to keep the energy going.](https://ko-fi.com/mbparks)



