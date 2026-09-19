# LaptopOverlayAR

A Unity-based augmented reality project for visualizing laptop hardware in 3D over a tracked image or AR surface. The repository combines Vuforia image tracking with Unity XR tooling to create a mobile AR experience that can place and manipulate computer components such as a motherboard, RAM, CPU, and GPU.

## Overview

This project is built as a Unity 6000 project and includes:

- AR Foundation / XR support for mobile AR
- Vuforia image tracking configured with a `Laptop_AR_DB` target database
- XR Interaction Toolkit for AR object interaction
- a starter-style AR UI flow for onboarding, object placement, and manipulation
- custom 3D hardware assets in `Assets/ARAssets`

The asset set includes models such as:

- `Assets/ARAssets/Motherboard.fbx`
- `Assets/ARAssets/RAM.fbx`
- `Assets/ARAssets/amd+ryzen+9+7950x.fbx`
- `Assets/ARAssets/cgt_gpu_001.fbx`

These assets strongly suggest the app is intended to showcase laptop internals in an interactive AR overlay.

## Key Features

- Image-targeted AR experience using Vuforia
- 3D hardware visualization for laptop components
- AR surface scanning and object placement workflows
- Object manipulation via move, rotate, and scale interactions
- Onboarding/tutorial UI for first-time users
- Mobile AR support through ARCore/ARKit integration

## Technology Stack

- Unity 6000.6.0f1
- AR Foundation
- XR Interaction Toolkit
- ARCore (`com.unity.xr.arcore`)
- ARKit (`com.unity.xr.arkit`)
- Vuforia (`com.ptc.vuforia.engine`)
- Universal Render Pipeline
- C# scripts for Unity scene logic and onboarding

## Repository Structure

```text
LaptopOverlayAR/
├── Assets/
│   ├── ARAssets/                 # 3D laptop-related models
│   ├── Editor/                   # Unity/Vuforia editor support
│   ├── MobileARTemplateAssets/   # AR template scripts, materials, UI, shaders
│   ├── Resources/                # Vuforia configuration assets
│   ├── Samples/                  # XR Interaction Toolkit samples
│   ├── Scenes/                   # Unity scene files
│   ├── Settings/                 # Project settings and AR configuration
│   └── XR/                       # XR resources and setup
├── Packages/
│   ├── manifest.json             # Unity package dependencies
│   └── packages-lock.json
├── ProjectSettings/
│   └── ProjectVersion.txt
├── LaptopOverlay.slnx           # Unity solution file
├── .gitignore
├── README.md
└── ...
```

## Notable Files

- `Packages/manifest.json` — declares the Unity packages and dependency graph for AR/XR support
- `Assets/MobileARTemplateAssets/Scripts/ARTemplateMenuManager.cs` — manages object menu, debug UI, AR plane visibility, and interaction state
- `Assets/MobileARTemplateAssets/Scripts/GoalManager.cs` — handles onboarding and user coaching flow
- `Assets/Editor/Vuforia/ImageTargetTextures/Laptop_AR_DB/` — contains the image target used by Vuforia
- `Assets/Resources/VuforiaConfiguration.asset` — Vuforia runtime configuration

## Getting Started

### Prerequisites

- Unity Hub
- Unity 6000.6.0f1 or compatible version
- Android/iOS device or emulator for AR testing
- Android Studio / Xcode depending on target platform

### Setup

1. Open the project in Unity.
2. Ensure the Unity packages in `Packages/manifest.json` are installed.
3. Open the main Unity scene under `Assets/Scenes` or the existing demo scene provided by the XR starter assets.
4. Connect an AR-capable device and build/run for Android or iOS.
5. If using the Vuforia image target workflow, make sure the target database and image asset are included in the build.
