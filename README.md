<p align="center">
  <img width="256" height="256" alt="YagaraIcon" src="https://github.com/user-attachments/assets/47c263c4-55f2-40ef-b91d-f1fbbaf6343b" />
</p>

<h1 align="center">YAGARA FLUID ENGINE</h1>

<p align="center">
  <b>High-Performance Real-Time 3D Fluid & Particle Simulation Engine</b><br>
  Powered by Vulkan 1.3 Compute & Data-Flow Node Graph System
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Version-0.1.2%20(Beta)-orange.svg?style=for-the-badge" alt="Version">
  <img src="https://img.shields.io/badge/Platform-Windows%20x64-blue.svg?style=for-the-badge&logo=windows" alt="Platform">
  <img src="https://img.shields.io/badge/Graphics-Vulkan%201.3-red.svg?style=for-the-badge&logo=vulkan" alt="Vulkan 1.3">
  <img src="https://img.shields.io/badge/C%2B%2B-20-00599C.svg?style=for-the-badge&logo=cplusplus" alt="C++20">
  <img src="https://img.shields.io/badge/Download%20Size-~4.9%20MB-brightgreen.svg?style=for-the-badge" alt="Size">
</p>

---

## 🌟 Overview

**Yagara Fluid Engine** is an ultra-fast, lightweight, standalone 3D visual effects and fluid simulation suite designed for technical artists, game developers, and VFX creators. 

Built from scratch in pure modern **C++20** and **Vulkan 1.3 Compute**, Yagara delivers real-time Navier-Stokes fluid dynamics (fire, smoke, explosions, combustion) coupled with millions of GPU particles and direct export pipelines to **Unreal Engine 5 (Niagara)**.

<p align="center">
  <img src="Yagara_load.png" alt="Yagara Splash Artwork" width="800">
</p>

---

## ✨ Key Features

### 🎛️ 1. Interactive Data-Flow Node Graph
- **True Visual Evaluation**: Niagara / Houdini-style procedural architecture where only connected nodes actively compute.
- **Rich Node Library**:
  - **Volume & Mesh Emitters**: Sphere, Box, Cylinder, Fuel & Smoke injectors.
  - **Fluid Physics & Solvers**: Buoyancy, Vorticity Confinement, Jacobi Pressure Projection, Multi-phase Combustion.
  - **Turbulence & External Forces**: 3D Curl Noise, Wind vectors, Gravity, Point Attraction/Repulsion.
  - **Dynamic Random Range**: Smooth Hermite curve, linear lerp, and stepped noise interpolation over customizable time intervals.
  - **Color & Absorption Gradients**: Multi-stop gradient ramps for temperature, smoke density, and flame emission.
- **Smart Wire Connection**: Intelligent quick-search menu when dragging wires onto empty canvas.
- **Step-by-Step Undo / Redo (`Ctrl+Z` / `Ctrl+Y`)**: Full history stack for node creation, deletions, links, and moves.

### 🔥 2. Real-Time 3D Navier-Stokes Fluid Solver
- GPU Voxel Grid simulation (128³, 256³ and beyond) computed entirely in parallel on Vulkan Compute pipelines.
- **Combustion Physics**: Real-time fuel consumption, ignition thresholds, heat transfer, and expansion.
- **High-Order Advection & Pressure Projection**: Stable fluids with minimal dissipation.

### ✨ 3. GPU Particle Physics Subsystem
- Simulates up to **100,000+ particles** in real time advected directly by the 3D fluid velocity field.
- Full control over lifespan, drag, turbulence injection, collision, size-over-life, and color decay.

### 🎥 4. Direct Volume Raymarching & Lighting
- Real-time raymarched volumetric absorption, emission, self-shadowing, and scattering.
- **First-Person Flycam** (RMB + WASD/QE) and Orbit navigation with customizable FOV.
- Light direction, ground grid, coordinate gizmo, and viewport performance metrics.

### ⏱️ 5. Timeline & Keyframe Animation
- Animate any simulation parameter (emitter radius, buoyancy, noise strength) across frames.
- Keyframe tracks, scrub playhead, loop controls, and curve interpolation.

### 🚀 6. Unreal Engine 5 VFX Pipeline
- **3D Vector Fields (`.FGA`)**: Export 3D fluid velocity fields ready for UE5 Niagara particle advection.
- **2D Flipbook Sprite Sheets**: Render animated 8x8 / 16x16 sprite sheets with optional normal maps.
- **OpenVDB Volume Grids**: Standard format for offline rendering and cinematic workflows.

---

## ⚡ Performance & Zero Dependencies

- **Microscopic Footprint**: The entire release package is only **~4.9 MB (ZIP)** / **~5.9 MB uncompressed**.
- **Instant Launch**: Starts in milliseconds with a Photoshop-style per-pixel alpha floating splash screen.
- **Zero Bloat**: No Python, no Electron, no Java runtime. Pure native x64 C++20 and Vulkan.

---

## 📥 Installation & Quick Start

### Minimum System Requirements
- **OS**: Windows 10 / 11 (64-bit)
- **GPU**: NVIDIA GeForce GTX 1060 / AMD Radeon RX 580 / Intel Arc or higher (Vulkan 1.3 support required)
- **RAM**: 4 GB+

### Running Yagara
1. Download **`Yagara_Release.zip`** from the [Latest Release](https://github.com/) page.
2. Extract the archive into any folder.
3. Launch **`YagaraFluidEngine.exe`**.

---

## 📂 Included Presets & Examples

- `projects/FireSparks_preset.yagara` — Multi-emitter fire with rising embers and turbulent smoke.
- `projects/CANDLE.yagara` — Micro-scale candle flame with laminar buoyancy.
- `projects/WINDSMOKE.yagara` — Dense smoke plume guided by directional vector wind and turbulence.

---

## 🛠️ Tech Stack & Third-Party Credits

Yagara Fluid Engine is made possible thanks to these open-source libraries:
- **Vulkan API** by *The Khronos Group Inc.*
- **Dear ImGui** by *Omar Cornut* (MIT License)
- **GLFW** by *Marcus Geelnard, Camilla Löwy* (zlib License)
- **GLM (OpenGL Mathematics)** by *G-Truc Creation* (MIT License)
- **volk** by *Arseny Kapoulkine* (MIT License)
- **Glslang** by *The Khronos Group Inc.* (BSD License)
- **TinyEXR & miniz** by *Syoyo Fujita, Rich Geldreich* (BSD & MIT License)
- **stb libraries** by *Sean Barrett* (Public Domain / MIT License)

---

<p align="center">
  <sub>Developed with ❤️ for the Computer Graphics and VFX Community.</sub>
</p>
