
<div align="center">
  <h1>SONISTO BEAT MACHINE</h1>
  
  <p>
    <strong>High-Fidelity Virtual Instrument & DSP Controller</strong>
  </p>

  <p>
    <a href="https://react.dev/">
      <img src="https://img.shields.io/badge/React_19-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
    </a>
    <a href="https://www.typescriptlang.org/">
      <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
    </a>
    <a href="https://vitejs.dev/">
      <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite" />
    </a>
    <a href="https://tailwindcss.com/">
      <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" />
    </a>
    <a href="https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API">
      <img src="https://img.shields.io/badge/Web_Audio_API-333333?style=for-the-badge&logo=w3c&logoColor=white" alt="Web Audio API" />
    </a>
  </p>
  
  <p>
    <a href="https://dovvnloading.github.io/Soisto-Beat-Machine">View Live Deployment</a>
  </p>
</div>

<br />

<div align="center">
  <img width="100%" alt="Sonisto Interface Main" src="https://github.com/user-attachments/assets/b21147a9-234d-42b1-b818-af1cbe96b58e" />
</div>

<br />

## Project Overview

Sonisto is a browser-based production environment designed to bridge the gap between physical hardware tactility and web-based DSP (Digital Signal Processing). Built on the Web Audio API and React 19, it features a neumorphic interface that replicates the weight and resistance of physical controls while offering immediate visual feedback.

The application serves as a 16-pad sampler, 8-channel mixer, and MIDI-compliant controller, capable of bidirectional communication with external hardware.

## Key Features

### Audio Engine & DSP
*   **16-Voice Polyphony:** Full sample playback capability across two banks (A/B).
*   **Per-Channel Processing:** Dedicated signal chain for every channel including Low-Pass Filter (Cutoff/Resonance), Drive (WaveShaper), and Pan.
*   **Global FX Send:** Integrated Convolver Reverb and Stereo Delay with tempo sync capabilities.
*   **Envelope Shaping:** Precise ADSR (Attack, Decay, Sustain, Release) + Tail control for every sample.

### Hardware Integration
*   **Web MIDI API:** Native support for external MIDI devices.
*   **MIDI Learn:** "Click-to-map" functionality allowing any on-screen knob or pad to be assigned to physical faders, knobs, or drumpads.
*   **Keyboard Support:** Low-latency keyboard mapping for laptop performance (Z-V, A-F).

### Visual Interface
*   **Real-Time Visualization:** Canvas-based frequency analyzer and oscilloscope.
*   **Neumorphic Design System:** CSS-driven lighting engines (shadows/highlights) that adapt to user interaction and theme switching.
*   **Dynamic Feedback:** LED states, active knob rotation, and fader tracking.

<br />

<div align="center">
  <img width="100%" alt="Sonisto Sampler View" src="https://github.com/user-attachments/assets/5cd51ce5-7f30-4fbf-8f3a-44b2a2bf93a8" />
</div>

<br />

## Technical Architecture

### Core Stack
*   **Framework:** React 19 (Functional Components, Hooks, Context).
*   **Build Tool:** Vite (ESBuild).
*   **Language:** TypeScript (Strict typing for DSP nodes and MIDI events).
*   **Styling:** Tailwind CSS (Utility-first, heavily customized with CSS variables for theming).

### Audio Pipeline
The audio graph utilizes `AudioContext` to manage a complex routing matrix:
1.  **Source:** `AudioBufferSourceNode` (Sample playback).
2.  **Gain:** Envelope shaping (ADSR).
3.  **Filter:** `BiquadFilterNode` (Lowpass).
4.  **Drive:** `WaveShaperNode` (Distortion algorithms).
5.  **Spatial:** `StereoPannerNode`.
6.  **Bus:** Master Compressor & Analyzer.

## Installation

Clone the repository and install dependencies locally.

```bash
git clone https://github.com/dovvnloading/Soisto-Beat-Machine.git
cd Soisto-Beat-Machine
npm install
```

### Development Server

Start the local Vite development server.

```bash
npm run dev
```

### Production Build

Compile TypeScript and generate static assets for deployment.

```bash
npm run build
```

## Usage Controls

### Computer Keyboard
*   **Triggers:** Keys `A`, `S`, `D`, `F` (Bottom Row) and `Z`, `X`, `C`, `V` (Top Row).
*   **Channel Selection:** Keys `1` through `8`.

### MIDI Mapping
1.  Click the **MIDI LEARN** button in the top header.
2.  The interface will desaturate, indicating mapping mode.
3.  Click an on-screen target (Knob or Pad).
4.  Move a physical control on your MIDI device.
5.  The connection is established instantly. Click **MIDI LEARN** again to exit.

## License

> This project is intended for educational and personal use. NOT for: copying and claiming as your own, mirroring or hosting your own version, duplicating repos, extracting ui stylies, or copying the engine.

---

<div align="center">
  <p><strong>Sonisto Audio • v0.3.4 PROTOTYPE</strong></p>
  <p>Design & Engineering by Matthew Robert Wesney</p>
</div>

