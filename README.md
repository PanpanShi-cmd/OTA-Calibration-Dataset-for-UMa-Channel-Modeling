# OTA Calibration Dataset for UMa Channel Modeling

## Overview

This repository provides research data supporting over-the-air (OTA) calibration and antenna characterization for ultra-massive MIMO (UM-MIMO) channel modeling in a 15-GHz urban macrocell (UMa) scenario. The release consists of **anechoic-chamber MIMO geometry** and **selected antenna radiation patterns**.

## Dataset Contents

### 1. Anechoic-Chamber MIMO Geometry

**File:** [`OTA_calibration_for_UMa/Chamber_MIMO_Geometry.mat`](OTA_calibration_for_UMa/Chamber_MIMO_Geometry.mat)

The MATLAB file describes the geometric configuration of the **128-element Tx array** and the **first 8-element Rx array plane** in the anechoic chamber. It contains the following variables:

| Variable | Size / type | Description |
| --- | --- | --- |
| `TXch` | 128 × 3 | Three-dimensional coordinates (X, Y, Z) of the 128 Tx elements, in meters. |
| `RXch` | 8 × 3 | Three-dimensional coordinates (X, Y, Z) of the 8 Rx elements, in meters. |
| `Gch` | MATLAB structure | Geometric information for all 128 × 8 = 1,024 Tx–Rx links, including link distances and propagation-angle information. |
| `R_Tx_ch` | 3 × 3 | Rotation matrix describing the Tx array orientation. |
| `R_Rx_ch` | 3 × 3 | Rotation matrix describing the Rx array orientation. |
| `angleStep_deg` | Scalar | Angular-step parameter used in geometry-related angle processing. |
| `patternAngleConvention` | Text | Angular convention used for radiation-pattern interpretation. |

The geometry represents this specific chamber configuration; it does not include the geometry of other Rx array planes.

### 2. Selected Antenna Radiation Patterns

**Directory:** [`OTA_calibration_for_UMa/Pattern/`](OTA_calibration_for_UMa/Pattern/)

The repository provides radiation-pattern data for **selected Tx/Rx antenna elements** at **three representative frequencies** and **multiple reference distances**:

| Parameter | Released data |
| --- | --- |
| Tx elements | 1, 33, and 64 (selected from 128 elements) |
| Rx elements | 1–8 |
| Frequencies | 14.875, 15.000, and 15.125 GHz |
| Reference distances | 1, 2, 3, 4.8, 74, 500, and 1,000 m |
| Angular sampling interval | 1° |
| File format | TXT |

The pattern files are organized by Tx/Rx element, frequency, and reference distance. For example:

`OTA_calibration_for_UMa/Pattern/Rx/element_1/14.875_GHz/element_1_1m_14.875_GHz.txt`

**These files are a representative subset of antenna radiation patterns, not a complete pattern database for every element, frequency, and distance.** The 1° value refers to the angular sampling interval of the released TXT files, not to antenna-pattern measurement accuracy. It should not be assumed to equal the `angleStep_deg` value stored in the geometry file.

## Scope

The repository provides the chamber geometry and a selection of antenna-pattern data used in the associated research. It does not contain the complete outdoor channel-measurement dataset or a full implementation of the channel-processing workflow.

## Citation

If you use this dataset in your research or publications, please cite this repository using the citation information provided in CITATION.cff.

Dataset: OTA Calibration Dataset for UMa Channel Modeling

Repository: https://github.com/PanpanShi-cmd/OTA-Calibration-Dataset-for-UMa-Channel-Modeling
