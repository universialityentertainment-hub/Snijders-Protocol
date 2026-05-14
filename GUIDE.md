# User Guide: Operating the QTC v2.2 Engine

## Introduction
The Quantum Time Calculator (QTC) v2.2 is designed for high-precision resonance locking. This guide explains how to initialize and verify the Diamond Geometry integrity.

## Quick Start
1. **Environment:** Ensure Python 3.x is installed.
2. **Execution:** Run `qtc_v2_2_master.py`.
3. **Observation:** The engine will automatically calculate the target frequency based on the thermal input (default 529 mK).

## Interpreting Output
* **Target Frequency:** This is the compensated resonance required for the Lu-Bi matrix.
* **Harshad Status [LOCKED]:** This confirms that the frequency is mathematically stable and divisible by its digit sum.
* **Integrity Hash:** Use this SHA-256 string to verify that the calculation has not been tampered with or corrupted by quantum drift.

## Advanced Calibration
To adjust for different environments, modify the `temp_mk` variable in the script. The engine will dynamically apply the Snijders Expansion Coefficients ($\alpha$ and $\beta$) to maintain the Zumkeller-lock.

​The Mirror Principle:
This code acts as a 'digital twin' or mirror of the physical Lu-Bi matrix. By running this calculator, the system creates a predictive model of thermal expansion. If the physical sensor data differs from the QTC-calculated frequency, the protocol identifies an entropic breach and initiates a Re-anchoring sequence.

---
*Note: Always verify the Sigma-Anchor (14880) before initiating full power transduction.*
