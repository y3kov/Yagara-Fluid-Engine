<p align="center">
  <img width="256" height="256" alt="YagaraIcon" src="https://github.com/user-attachments/assets/47c263c4-55f2-40ef-b91d-f1fbbaf6343b" />
</p>

<h1 align="center">YAGARA FLUID ENGINE</h1>

<div align="center">

[![Discord](https://img.shields.io/badge/Discord-Join%20Server-5865F2?style=for-the-badge&logo=discord&logoColor=white&labelColor=2C2F33&logoSize=auto)](https://discord.gg/mPZPjGvNk)

<p align="center">
  <b>High-Performance Real-Time 3D Fluid, Liquid & Particle Simulation Engine</b><br>
  Powered by Vulkan 1.3 Compute & Strict Data-Flow Node Graph Architecture
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Version-0.1.4%20(Beta)-orange.svg?style=for-the-badge" alt="Version">
  <img src="https://img.shields.io/badge/Platform-Windows%20x64-blue.svg?style=for-the-badge&logo=windows" alt="Platform">
  <img src="https://img.shields.io/badge/Graphics-Vulkan%201.3-red.svg?style=for-the-badge&logo=vulkan" alt="Vulkan 1.3">
  <img src="https://img.shields.io/badge/C%2B%2B-20-00599C.svg?style=for-the-badge&logo=cplusplus" alt="C++20">
  <img src="https://img.shields.io/badge/Download%20Size-~4.9%20MB-brightgreen.svg?style=for-the-badge" alt="Size">
</p>

</div>

---

## 🌟 Overview

**Yagara Fluid Engine** is an ultra-fast, lightweight, standalone 3D visual effects and fluid simulation suite designed for technical artists, game developers, and VFX creators. 

Built from scratch in pure modern **C++20** and **Vulkan 1.3 Compute**, Yagara delivers real-time Navier-Stokes fluid dynamics (fire, smoke, explosions, combustion), SPH liquid & water simulation (Smoothed Particle Hydrodynamics with Screen Space Fluid Rendering), millions of GPU particles, and direct export pipelines to **Unreal Engine 5 (Niagara)**.

<p align="center">
<img width="540" height="541" alt="fireL" src="https://github.com/user-attachments/assets/cd4cae44-f230-4b50-a96d-40eef625a633" />
</p>

---

## ✨ Key Features

### 🎛️ 1. Interactive Data-Flow Node Graph
- **True Visual Evaluation**: Niagara / Houdini-style procedural architecture where only connected nodes actively compute.
- **Rich Node Library**:
  - **3D Geometry & Shapes**: Procedural 3D primitives (Sphere, Box, Cylinder, Cone, Torus, Disc, Candle Flame, Capsule) and custom 3D mesh assets.
  - **Volume & Mesh Emitters**: Density, heat, fuel, and velocity injectors.
  - **SPH Liquid Solver**: 3D smoothed particle hydrodynamics liquid physics with GPU-accelerated sorting.
  - **Navier-Stokes Gas & Combustion**: Buoyancy, Vorticity Confinement, Pressure Projection, and multi-phase chemical combustion.
  - **Turbulence & Multi-Force Fields**: Up to 4 simultaneous force fields (3D Curl Noise, Wind vectors, Gravity, Point Attraction/Repulsion).
  - **GPU Particle System**: Spawners, physics dynamics, and customizable PBR / Bloom renderers.
  - **Rigid Body Colliders**: Solid physical obstacles with friction, bounciness, and heat transfer.
- **Smart Drag & Drop Wiring**: Intelligent context menu when dragging wires onto empty canvas.
- **Step-by-Step Undo / Redo (`Ctrl+Z` / `Ctrl+Y`)**: Full history stack for node creation, deletions, links, and moves.

### 🔥 2. Real-Time 3D Navier-Stokes Fluid Solver
- GPU Voxel Grid simulation (128³, 256³ and beyond) computed entirely in parallel on Vulkan Compute pipelines.
- **Combustion Physics**: Real-time fuel consumption, ignition thresholds, heat transfer, and expansion.
- **High-Order Advection & Pressure Projection**: Stable fluids with minimal dissipation.

### 🌊 3. SPH Liquid Simulation & Screen Space Fluid Rendering (SSFR)
- **Real-Time 3D GPU Liquid Solver**: High-performance liquid dynamics with advanced pressure stabilization, natural viscosity, and anti-explosion safeguards.
- **Screen Space Fluid Rendering (SSFR)**: Photorealistic water surface reconstruction with edge-preserving bilateral depth filtering, surface normal extraction, physical light absorption, and Fresnel reflection/refraction.
- **Volumetric Scatter & Velocity Gradients**: 3D density voxelization with volume raymarching and dynamic speed-based color ramps.

### 🧊 4. Universal 3D Asset Pipeline (FBX, OBJ, STL, PLY)
- **Native Autodesk FBX Support**: Built-in support for FBX (Binary & ASCII), Wavefront OBJ, STL, and PLY formats without external plugins.
- **Accurate Transformations**: Preserves complex pivot hierarchies, multi-axis rotations, and proportions as authored in Blender, Maya, or 3ds Max.
- **Drag & Drop Import**: Drag 3D models directly into the viewport for automatic node graph generation (Shape $\to$ Collider / Emitter / Particles).
- **Smart Adaptive 3D Volumes**: Automatic topology detection for solid objects (closed volumes) and thin-shell architecture (walls, roofs, open containers) with hardware depth and particle occlusion.

### ✨ 5. GPU Particle Physics Subsystem
- Simulates up to **100,000+ particles** in real time advected directly by the 3D fluid velocity field.
- Full control over lifespan, drag, turbulence injection, collision, size-over-life, and color decay.
- Multiple visual styles: Sparks / Embers, Soft Billboards, Motion Streaks, Glowing Plasma, and physically shaded 3D PBR Spheres.

<img width="320" height="240" alt="TestMesh_Prticle (1)" src="https://github.com/user-attachments/assets/9c9d0cae-389f-40da-9622-2194b275f621" /> <img width="320" height="240" alt="2026-08-28 230358" src="https://github.com/user-attachments/assets/8c097ec6-cd4f-44cd-b6d2-368902e4d11a" /> <img width="320" height="240" alt="Запись экрана 2026-08-28 040115" src="https://github.com/user-attachments/assets/71defee5-d301-4993-83f1-28379e0718ca" />





### 📐 6. Industry-Standard Z-Up Coordinate System
- Fully aligned with modern game engines (Unreal Engine 5: +Z Up, +X Forward, +Y Right).
- Unified procedural 3D math and rotation pipelines across the engine and viewport.
- Automatic coordinate conversion for imported 3D assets.

### 🎥 7. Direct Volume Raymarching & Lighting
- Real-time raymarched volumetric absorption, emission, self-shadowing, and scattering.
- **First-Person Flycam** (RMB + WASD/QE) and Orbit navigation with customizable FOV.
- **World Settings Panel**: Quality presets (Fast, Balanced, High, Custom) and dynamic **Render Resolution Scale** slider for instant GPU performance tuning.

### ⏱️ 8. Timeline & Keyframe Animation
- Animate any simulation parameter (emitter radius, buoyancy, noise strength) across frames.
- Keyframe tracks, scrub playhead, loop controls, and curve interpolation.

### 🚀 9. Unreal Engine 5 VFX Pipeline
- **3D Vector Fields (`.FGA`)**: Export 3D fluid velocity fields ready for UE5 Niagara particle advection.
- **2D Flipbook Sprite Sheets**: Render animated 8x8 / 16x16 sprite sheets with optional 16-bit HDR (.EXR) support.
- **OpenVDB Volume Grids**: Standard format for offline rendering and cinematic workflows.

---

<p align="center">
<img width="3439" height="1389" alt="Yagara UI Overview" src="https://github.com/user-attachments/assets/82647936-f482-4495-adca-39e8f28bd23e" />
</p>

---

## ⚡ Performance & Zero Dependencies

- **Microscopic Footprint**: Standalone executable is only **~2.1 MB**; entire release package is **~4.9 MB (ZIP)**.
- **Instant Launch**: Starts in milliseconds with a Photoshop-style per-pixel alpha floating splash screen.
- **Zero Bloat**: No Python, no Electron, no Java runtime. Pure native x64 C++20 and Vulkan 1.3 Compute.

---

## 📥 Installation & Quick Start

### Minimum System Requirements
- **OS**: Windows 10 / 11 (64-bit)
- **GPU**: NVIDIA GeForce GTX 1060 / AMD Radeon RX 580 / Intel Arc or higher (Vulkan 1.3 support required)
- **RAM**: 4 GB+

### Running Yagara
1. Download **`Yagara.v0.1.4.beta.zip`** from the [Latest Release](https://github.com/y3kov/Yagara-Fluid-Engine/releases) page.
2. Extract the archive into any folder.
3. Launch **`YagaraFluidEngine.exe`**.

---

## 📂 Included Presets & Examples

- `projects/SPH_Water.yagara` — 3D SPH liquid simulation with Screen-Space Fluid Rendering (SSFR).
- `projects/Fire+Particle+Collision.yagara` — High-temperature combustion fire, rising sparks, and solid obstacle collision.
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
