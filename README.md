# Optical-Time-Domain-Reflectometer-OTDR-measurement-using-AFL-M200
This exercise documents the testing and evaluation of several single-mode fiber optic links using the **AFL M200 OTDR (Optical Time Domain Reflectometer)**. The primary objective was to detect and analyze splices, connectors, and faults within the fiber infrastructure. Tests were conducted on multiple fiber segments, including both individual and concatenated fiber links.

---

## 🧠 Introduction

In optical networks, maintaining the integrity of fiber links is critical for signal quality and system uptime. OTDR is an electronic measuring device used to
qualitatively and quantitatively assess events occurring in a fiber optic path. They are essential tools for commissioning, troubleshooting, and certifying optical links. The AFL M200 was used to assess the performance of five fiber strands. Some showed continuity and signal integrity, while others revealed splices with high losses or discontinuities.

Phenomena occurring in fibers include: Rayleigh scattering, reflection at splice locations, Fresnel reflection at the beginning and end of the fiber, and at the junction of two fibers(connectors), dead zones, and ghosting. 

---

## ⚙️ Principle of Operation

An OTDR sends short laser pulses into a fiber and measures the backscattered light as a function of time. The device's operating principle is based on the analysis of the returned signal, which may be reflected from the fiber end or other discontinuities in the fiber (connector), or backscattered by inhomogeneities within the fiber. It uses this information to estimate:
- Fiber length
- Event location (splices, connectors, breaks)
- Insertion loss
- Reflectance

The AFL M200 operates in Full Auto Mode, which:
- Automatically sets test parameters (range, pulse width, averaging)
- Generates event tables and summary reports
- Allows quick detection of faults and performance issues

Key technical specs for the AFL M200:
- Dynamic range**: 26 dB (single-mode)
- Event dead zone: 1.5 m
- Attenuation dead zone: 9 m
- Wavelengths: 1310/1550 nm
- Resolution: 0.25 m to 1 m depending on range
- [Full specifications →](https://www.aflglobal.com/Products/Test-and-Inspection/OTDR/M200.aspx)

---

## 🔧 Test Setup

- Device: AFL M200 OTDR
- Mode: Full Auto
- Fiber type: Single-mode
- Launch/Receive cables: Used as required for accurate end-to-end loss measurement

---

## 📊 Results Summary

## Fiber Links 1 and 4 (Single fibers)
The initial visual inspection showed that optical fibers no. 1 and 4 were not conductive, so they were not further analyzed.

### Fiber Link 2

[Full specifications →](https://www.aflglobal.com/Products/Test-and-Inspection/OTDR/M200.aspx)

| # | Event Type | Distance (km) | Loss (dB) |
|---|------------|----------------|-----------|
| 1 | Splice     | 0.1807         | 2.023     |
| 2 | Splice     | 0.3849         | 0.960     |

🛠️ High loss on Splice 1 suggests poor fusion or dirty end-faces.

---

### Fiber Segment 3
[Full specifications →](https://www.aflglobal.com/Products/Test-and-Inspection/OTDR/M200.aspx)
| # | Event Type | Distance (km) | Loss (dB) |
|---|------------|----------------|-----------|
| 1 | Splice     | 0.7106         | 1.162     |

---

### Fiber Segment 5
[Full specifications →](https://www.aflglobal.com/Products/Test-and-Inspection/OTDR/M200.aspx)
- ✅ No events detected
- 🧪 Indicates clean, continuous fiber

---

### Combined Link: Segment 3 + 5 + 2
[Full specifications →](https://www.aflglobal.com/Products/Test-and-Inspection/OTDR/M200.aspx)
| # | Event Type | Distance (km) | Loss (dB) |
|---|------------|----------------|-----------|
| 1 | Connector  | 1.4510         | 0.436     |
| 2 | Connector  | 1.7722         | 0.092     |
| 3 | Splice     | 1.9675         | 1.882     |
| 4 | Splice     | 2.1728         | 2.1728    |

🧭 **Observation**: One previously detected splice from Segment 3 disappeared — likely due to **dead zone overlap** in the merged trace.

---

## 🧩 Key Terms

- **Splice**: Permanent joint between fibers (fusion). Minimal reflection if done correctly.
- **Connector**: Temporary joint. Reflective due to air gap or misalignment.
- **Dead Zone**: Region where nearby events can’t be resolved separately (M200: 1.5–9 m depending on type).
- **Ghost**: False reflection due to multiple reflections or high reflectance events.
- **Insertion Loss (IL)**: Power lost between two points on the fiber. Measured in dB.

---

## ✅ Conclusion

- Splices in Segments 2 and 3 showed **moderate to high losses**, suggesting inspection or rework is needed.
- Segment 5 passed with no events.
- Combined testing validated continuity but highlighted compounded losses and dead zone limitations.
- The AFL M200 OTDR proved effective for link verification, fault location, and quality assurance.

---

## 📍 Author

**Samuel Oluwafemi Oladosu**  
*Fiber Optic Link Testing with AFL M200*
