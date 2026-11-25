# NVSmooth v1.0

**NVSmooth** is a lightweight, standalone Windows utility that applies an optimized global profile to NVIDIA drivers in a single click, designed to eliminate micro-stuttering, stabilize *frametimes*, and improve overall gaming smoothness.

It communicates directly with the native driver library (`nvapi64.dll`), so it **does not require NVIDIA Profile Inspector** or any third-party software to be installed.

<img width="1408" height="768" alt="NVSmooth v1 0" src="https://github.com/user-attachments/assets/48c6dd7d-2cc2-46da-bbfa-d5ec8292bfb8" />

## Key Features

* **Zero Dependencies:** Single ready-to-use executable file (`NVSmooth.exe`).
* **Safe & Verifiable:** Executable digitally signed by the author (`Igor Borgacci (ilborga70)`).
* **Broad Compatibility:** Works on all NVIDIA GPUs on Windows 10/11 (64-bit). On older cards (e.g., GTX series without DLSS support), the tool automatically applies all compatible optimizations while safely ignoring RTX-only parameters.

---

## Driver Optimizations Applied

| Setting | Applied Value | In-Game Benefit |
| :--- | :--- | :--- |
| **Shader Disk Cache Size** | `100 GB` | Prevents continuous shader deletion and recompilation, eliminating *shader compilation stutter*. |
| **Vertical Sync + Tear Control** | `Force On` + `Adaptive` | Eliminates screen *tearing* when reaching monitor refresh rate and instantly disables V-Sync if FPS drops below the threshold, preventing abrupt framerate halving. |
| **Power Management Mode** | `Prefer Maximum Performance` | Keeps GPU clock speeds stable, preventing micro-stutters caused by power state transitions (*P-States*). |
| **Global G-SYNC / VRR** | `Disabled` | Works alongside Adaptive V-Sync and eliminates *VRR flicker* (brightness flickering) on OLED and VA panels. |
| **Preferred Refresh Rate** | `Highest Available` | Forces applications to always use the maximum refresh rate supported by your monitor. |
| **FRL Low Latency** | `On` | Reduces the render queue and keeps input lag to a minimum when hitting the frame rate cap. |
| **DLSS Overrides (RTX Only)** | `Quality Preset` + `Latest` | Forces the latest driver-level DLSS libraries (SR, RR, FG) in Quality mode to lower GPU load and stabilize frametimes. |

---

## How to Use

1. Download the latest release (`NVSmooth_v1.0.zip`) from the **[Releases](../../releases)** section.
2. Extract the archive and close any running games or 3D applications.
3. Double-click **`NVSmooth.exe`** and accept the Windows User Account Control (UAC) prompt.
4. Wait for the confirmation message *"Profilo applicato con successo!"* (Profile applied successfully!).

> **Windows SmartScreen Note:** Because this is an independent executable with a self-signed digital certificate, Windows may display a warning on first launch. Click **"More info"** -> **"Run anyway"** (you can verify the `Igor Borgacci (ilborga70)` digital signature in the file Properties).

---

## Restoring Default Settings

If you ever wish to revert to the standard NVIDIA configuration:
1. Open the **NVIDIA Control Panel** (right-click on your Desktop).
2. Go to **Manage 3D settings** -> **Global Settings** tab.
3. Click the **Restore** button and confirm with **Apply**.

---

### 🔬 Is this file 100% safe?
Yes! If you are worried about security, the file has been fully analyzed on Jotti's malware scan. The results show 0/13 scanners reporting malware, meaning top antiviruses like Kaspersky, BitDefender, and Avast found absolutely nothing.

### 🔒 Antivirus False Positives
Since the file was compiled using Win-PS2EXE, any alerts are due to the nature of the compiler wrapper. Don't worry — the code has been reviewed by IT experts and has been found to be completely safe and clean.

🔗 **Check the full safety report here:** [Jotti's Malware Scan Report](https://virusscan.jotti.org/it-IT/filescanjob/te6x26nq8t)

---

## Author

Created and optimized by **Igor Borgacci (`ilborga70`)**.
