# Starship ASMR Simulator

**A browser-based ambient starship cockpit experience designed for relaxation, immersion, and creative production.**

*Authored by M.B. Parks*

---

## What Is This?

This is not a game. There are no objectives, no scores, no fail states.

Starship ASMR Simulator is a single HTML file that transforms your browser into the cockpit of a deep-space vessel. It's designed to run in full screen alongside ambient audio — particularly space traffic control and starship ambience tracks — to create an immersive, calming experience that feels like sitting at the helm of a ship cruising through interstellar space.

**Recommended audio pairing:** [Space Traffic Control ASMR](https://www.youtube.com/watch?v=-q4XwtdSxDE)

**Try it here: https://mbparks.com/starship

### Use Cases

- **ASMR / Ambient Relaxation** — Run it full screen with headphones. The engine hum, soft console blips, and occasional radio chatter create a deeply calming soundscape. Interact as much or as little as you want.
- **Film & Video Production** — Need a convincing cockpit display for a short film, YouTube video, or stream overlay? This provides a realistic, animated starship interface with working readouts, comms chatter, and interactive systems.
- **Streaming Background** — Use it as an animated backdrop for podcasts, lo-fi streams, or creative work sessions.
- **Worldbuilding & Creative Writing** — Writers working on science fiction can use this as an ambient writing environment that keeps them in the headspace of their story.
- **Focus / Study Aid** — The gentle hum and slow-moving starfield provide a non-distracting ambient environment for deep work.

---

## Quick Start

1. Download `starship-cockpit.html`
2. Open it in any modern browser (Chrome, Firefox, Edge, Safari)
3. Name your ship and select a difficulty profile
4. Click **Engage Systems**
5. Press **F** or double-click for full screen
6. Pair with your favorite space ambient audio

No server, no dependencies, no build step. It's a single self-contained HTML file.

---

## Features

### 🌌 Viewport & Starfield

- **3D forward-flying starfield** with parallax depth — stars fly toward you from a central vanishing point, growing larger and brighter as they approach
- **Star color variation** — white-blue, warm yellow, cool blue, pale orange, and rare pale red stars
- **Nebula clouds** with slow drift and occasional lightning/energy discharges deep within the formations
- **Comets** with glowing tails that cross the viewport every 10–15 minutes
- **Asteroids** — tumbling irregular rocks with procedural shapes
- **Distant ships** with blinking red/green navigation lights
- **Planets** with lit-side gradient shading that slowly drift across the viewport
- **Bioluminescent space organisms** — glowing jellyfish-like creatures that rarely appear in clusters, pulsing with soft light, with trailing tentacles. Fully scannable.
- **CRT scanline overlay** and **vignette** darkening at the edges for a cockpit glass feel
- **Lens flare** when bright stars pass near viewport center
- **Mouse parallax** — cockpit bezel elements shift subtly with mouse movement, creating physical depth
- **Condensation drips** — tiny droplets occasionally form and slide down the viewport edges
- **Starfield density variation** — star count gradually shifts over time, simulating denser and sparser regions of space
- **Day/night cockpit cycle** — ambient glow slowly shifts between cool blue and warm amber over ~10 minutes

### 🎛️ Cockpit Interface

- **Top panel** — System status bars for Shields, Reactor, O₂, Comms, Nav, and Gravity with animated progress bars
- **Left panel** — 9 toggle switches (EXT, NAV, COM, SHD, LIF, WPN, SEN, AUX, EMR) with LED indicators, tooltips, and click sounds
- **Right panel** — Live readouts for Distance, ETA, Crew count, Cargo, Radiation, Signal strength, and Drift
- **Bottom console** — HUD data (Velocity, Heading, Hull Temp, System, Fuel Cell, Pressure), 7 console buttons with LED indicators, volume slider, throttle slider, and control buttons
- **Nav compass** — Rotating needle tracking current heading
- **Oscilloscope waveform** — Animated signal display that responds to throttle setting
- **Radar/lidar display** — Circular sweep with rotating scan line and blips for nearby objects
- **Mission clock** — Accelerated elapsed time display (100x real time)
- **Crew activity log** — Scrolling ticker of crew events with captain's log input
- **Fuel consumption graph** — Real-time line chart tracking fuel cell percentage
- **Space weather radar** — Flowing visualization of solar wind, radiation belts, and magnetic field lines with real effects on ship systems
- **System status grid** — Clickable status indicators for 8 subsystems with detailed popup panels showing specs, uptime, live component data, and performance graphs
- **Panel wear texture** — Subtle grain and scratch effects on bezel surfaces

### 🔊 Audio (Web Audio API)

All audio is procedurally generated — no external files required.

- **Engine hum** — Layered sine/triangle/sawtooth oscillators at 42–84 Hz with slow LFO modulation. Toggleable via the Engine button.
- **Air circulation hiss** — Filtered white noise simulating life support airflow
- **Console blips** — Soft randomized sine pings every 15–30 seconds
- **Radio static bursts** — Bandpass-filtered noise preceding each radio transmission
- **Scanner pings** — Descending frequency sweep when clicking the starfield
- **Button click sounds** — Soft sine pips for all interface interactions
- **Warp sounds** — Rising/falling sawtooth with lowpass filter for FTL engagement
- **Proximity alert** — Gentle two-tone alarm when asteroids pass close
- **Weapons sounds** — Laser fire (adjustable pitch by frequency setting), torpedo whoosh, impact rumbles
- **Tractor beam hum** — Sustained tone during lock
- **Various system sounds** — Restart whines, scan sweeps, hail connection tones, distress SOS morse

### 📡 Communications

- **Radio chatter** — 20+ procedural radio messages from Artemis Control, cargo vessels, science ships, patrol craft, automated beacons, and unknown signals. Messages appear every 20–60 seconds.
- **Radio reply system** — When messages arrive, 2–3 contextual reply options appear. Selecting one logs your response and occasionally triggers a follow-up message from the sender.
- **Hail system** — Open a channel to any of 10+ known contacts or ships detected on sensors. Full multi-turn conversations with procedural responses covering status, heading, trade, news, and anomaly reports. Weak-signal contacts have longer connect times and a chance of connection failure.
- **Comms log** — Full scrollable transcript of all radio traffic and captain's log entries
- **Captain's log input** — Type entries that appear in the crew activity ticker and comms log
- **Ship's AI terminal** — Type commands (`status`, `scan`, `crew`, `eta`, `fuel`, `shields`, `heading`, `log`, `help`) for typewriter-style procedural responses
- **Distress signal** — Covered SOS toggle with safety flap animation. Activating turns edge glows red, plays repeating SOS morse, and broadcasts an emergency message.

### 🗺️ Navigation & Helm

- **Star map** — Toggleable constellation/waypoint overlay with sector grid
- **Navigation planner** — Interactive chart where you click waypoints to plot multi-leg routes with estimated distance, fuel cost, and feasibility warnings
- **Helm control** — Full-screen translucent overlay with:
  - Course input (Bearing 0–360°, Mark -90 to +90° in Star Trek style, Velocity in fractions of c)
  - "Engage" button with confirmation sound and comms log entry
  - Attitude control (Yaw, Pitch, Roll sliders that spring back to center)
  - Live heading readouts
- **Click-and-drag pan** — Drag the starfield to shift your view with rubber-band return
- **Warp drive** — Stretches stars into radial streaks with rising engine pitch

### 🔬 Science & Exploration

- **Object scanning** — Hover any space object and click "Scan" for a 3-second analysis with progress bar and sweep sound. Returns a data card with procedurally generated composition, mass, temperature, origin, and threat level. Organisms get extra fields (bioluminescence color, colony size, species classification).
- **Deep scan probe** — Launch a sensor probe toward a random target. 60-second transit with countdown timer. Returns standard, notable (22% chance), or exceptional findings (8% — alien artifacts, first contact evidence).
- **Signal decryption** — When "Unknown Signal" messages appear, an "Attempt Decrypt" puzzle opens. Adjust three frequency dials to align your waveform with the target. Solving it reveals cryptic message fragments that accumulate across your session, building a mystery about ancient beacons and alien structures.
- **Nebula sample collection** — When passing near a nebula, deploy a collector for 30 seconds. Returns a spectrographic analysis card with classification, elemental composition, emission spectrum visualization, and scientific findings.
- **Discovery log** — Persistent archive of all scanned objects, probe returns, decoded signals, and collected samples

### 🔧 Engineering

- **Real-time animated graphs** — 7 systems (Reactor, Coolant, Hull, Shields, Life Support, Port Thruster, Starboard Thruster) with continuously scrolling data. Configurable time windows (30s, 1m, 5m).
- **Per-system power cycling** — Take any system offline for 5 seconds to clear faults
- **Component deep-dive** — Expand any system to see 8 individual components with OK/FAULT status. Replace faulty components individually.
- **Bypass routing** — When degraded, reroute through backup systems with described tradeoffs
- **Efficiency tuning** — Per-system Longevity ↔ Performance slider affecting output and wear
- **Alert threshold configuration** — Adjustable amber/red warning levels per system
- **Maintenance history** — Scrollable log of all repairs, restarts, and component replacements
- **Automated recommendations** — Context-aware suggestions based on system state and repair frequency

### ⚡ Power Management

- **Power allocation grid** — 5 systems (Engines, Shields, Sensors, Life Support, Weapons) sharing 500 total reactor units
- **Real effects** — Engine power controls throttle, shield power controls deflector strength, life support power controls O₂
- **Overload system** — Push any system above 130% for boosted performance with burnout risk (40–70% chance after 8–20 seconds). Burned-out systems go offline for 15 seconds.
- **Auto-redistribution** — Sliding one system up proportionally reduces others

### 🚀 Ship Systems

- **Deck schematic** — Interactive 4-deck, 16-room ship layout with crew positions. Click any room for detailed info (atmosphere, power draw, occupants, description). Room-specific actions: Med Bay bio-scan, Cargo inventory check, Armory security protocol, Cryo Bay crew wake sequence.
- **Bulkhead controls** — Click between rooms to lock/unlock bulkhead doors for atmosphere containment
- **Crew manifest** — 6 crew members with roles, locations, heart rates, and status (including one in cryo)
- **Exterior cameras** — 4 camera feeds (Forward, Port, Starboard, Aft) with directional star drift and occasional static on Camera 4
- **PIP aft camera** — Draggable picture-in-picture window showing stars streaming away
- **Mission objectives** — Checklist with completed, active, and pending objectives

### 🔫 Weapons

- **Tactical viewport** — Full targeting display with grid overlay, center crosshair, and mouse-tracking reticle
- **Target lock** — Click contacts to acquire lock with animated corner brackets, pulsing ring, and lock tone
- **Laser array** — Adjustable intensity (10–100%), frequency (IR through Gamma), and mode (Pulse/Beam). Heat management system with overheat cooldown. Visual beam/pulse effects with impact flashes.
- **Torpedo bay** — 8-tube rack with visual loaded/fired indicators. Torpedoes travel visually to target with green trail and explosion effect on impact. 85% hit chance, heavy damage.
- **Shield distribution** — 3×3 directional grid (8 sectors). Click to reinforce any sector by drawing from adjacent ones.
- **Weapons log** — Timestamped record of all hits, misses, launches, and destructions

### 🛡️ Emergency Systems

- **Emergency override panel** — Reactor Scram (dims all systems for 8s), Emergency Vent (drops pressure with rushing air sound), Thruster Override (ship shakes for 5s with thruster bursts)
- **Maintenance events** — Periodically a system degrades with notification. Ignore for 60s and it goes critical with cascading failures. Run a 4-step diagnostic repair sequence to fix.
- **Proximity alerts** — Amber bezel flash with two-tone alarm when asteroids pass close
- **Tractor beam** — Arm and lock onto asteroids or bio creatures. Visible beam connects ship to target. Release to cargo bay or set adrift.

### ⚙️ Configuration

- **Ship naming** — Name your vessel on first load. Persists via localStorage. Replaces "ISS Artemis" throughout all interfaces, radio callsigns, and database entries.
- **Difficulty presets:**
  - **Peaceful Cruise** — No malfunctions, no burnout risk. Pure ambient experience.
  - **Standard Patrol** — Balanced events and maintenance.
  - **Deep Frontier** — Frequent events, faster escalation, higher burnout risk.
- **Audio mixer** — Individual sliders for engine hum, air circulation, console blips, radio chatter frequency, and ambient drone
- **End of watch summary** — Formatted session report covering navigation, operations, communications, engineering, and mission stats

---

## Controls

| Action | Control |
|--------|---------|
| Full screen | Press `F` or double-click |
| Pan starfield | Click and drag |
| Scanner ping | Click starfield |
| Scan object | Hover object → click "Scan" |
| Hail ship | Hover ship → click "Hail" |
| Volume | Bottom-right slider |
| Throttle | Bottom-right amber slider |
| Warp | Bottom-right "Warp" button |
| Engine mute | Bottom-right "Engine" button |
| Captain's log | Type in bottom-right input, press Enter |
| All screens | Toggle bar above bottom console |

---

## Technical Details

- **Single file** — Everything is contained in one HTML file. No external dependencies, no build tools, no server required.
- **Web Audio API** — All sound is procedurally generated at runtime using oscillators, noise buffers, and filters.
- **Canvas rendering** — Starfield, radar, oscilloscope, space weather, cameras, weapons viewport, and all graphs rendered on HTML5 canvas elements.
- **CSS-only cockpit** — Bezel, panels, glows, and UI elements are pure CSS with clamp() responsive sizing.
- **~5,700 lines** — Entirely self-contained HTML/CSS/JavaScript.
- **60fps animation** — Uses requestAnimationFrame with efficient rendering.
- **localStorage** — Ship name and difficulty persist across sessions.
- **No frameworks** — Vanilla JavaScript throughout. No React, no libraries, no dependencies.

### Browser Compatibility

Tested and working in:
- Chrome 90+
- Firefox 90+
- Edge 90+
- Safari 15+

---

## Recommended Setup

For the best experience:

1. Use a large monitor or TV
2. Go full screen (`F` key)
3. Dim your room lights
4. Put on headphones
5. Open the [recommended audio](https://www.youtube.com/watch?v=-q4XwtdSxDE) in another tab
6. Adjust the in-simulator volume to complement the external audio
7. Select **Peaceful Cruise** for pure relaxation, or **Standard Patrol** if you want occasional ship activity

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
- Use **Peaceful Cruise** mode to prevent disruptive maintenance alerts during takes

---

## License

This project is provided as-is for personal, creative, and educational use.

---

*Built with care for anyone who's ever looked up at the stars and imagined what it would be like to be out there.*
