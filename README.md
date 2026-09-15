# Image-Based SPC Control Charts for Robotic LFAM Extrusion

Statistical process control (SPC) pipeline for real-time, image-based defect detection in
**Large Format Additive Manufacturing (LFAM)** via robotic polymer composite extrusion , a
process relevant to in-space and autonomous manufacturing, where human inspection is not
available and material waste cannot be tolerated.

Developed for the *Quality Data Analysis* course at Politecnico di Milano (AY 2025–2026).

## What it does

- **Layer detection & feature extraction** from extrusion images (OpenCV / scikit-image)
- **PCA-based monitoring statistics** to reduce high-dimensional image features into
  control-chart-ready signals
- **Statistical assumption checking** (normality, independence) required for valid SPC
- **Phase 1 control chart design**: baseline construction and control limit estimation
- **Phase 2 validation**: testing the proposed monitoring approach on unseen data, with an
  IMR (Individuals–Moving Range) chart benchmark for comparison

## Tech stack

Python — `numpy`, `pandas`, `scipy`, `scikit-learn` (PCA), `opencv-python`, `scikit-image`,
`matplotlib`

> **Note:** the notebook also imports `qdatoolkit`, a helper package provided as course
> material for Quality Data Analysis and not publicly available on PyPI. The core
> methodology (feature extraction, PCA monitoring, control charts) is implemented directly
> in the notebook and does not depend on proprietary logic from that package — it is used
> mainly for course-specific plotting/data utilities.

## Structure

- `Phase 1`: introduction, exploratory data analysis, statistical assumption checks,
  proposed methodology (parameter setting → feature extraction → PCA monitoring →
  interpretation/visualization), performance metrics, results
- `Phase 2`: validation of the Phase 1 approach on new data, IMR benchmark comparison,
  discussion and final summary


## Author

Giuseppe Salerno — salernog009@gmail.com  https://www.linkedin.com/in/giuseppe-salerno-461323364/

