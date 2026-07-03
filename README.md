# colour-grade-denoising
Comparative evaluation of nine image denoising methods for colour-grade preservation in graded cinematic footage, using ∆E2000 as a perceptual fidelity metric.
# Colour-Grade Preservation in Image Denoising

BSc Mathematics & Physics dissertation project comparing nine image 
denoising methods for their ability to preserve cinematic colour grading, 
evaluated across five LUTs and three noise levels.

## Overview

Standard denoising evaluation relies on PSNR/SSIM, which measure pixel-level 
accuracy but not perceptual colour fidelity. This project introduces 
ΔE2000 (perceptual colour difference) as a primary evaluation metric 
alongside PSNR/SSIM, revealing that several high-PSNR methods actively 
degrade colour grade fidelity on graded footage.

## Methods compared

- **Iterative solvers:** Jacobi, Gauss-Seidel
- **Fourier filtering**
- **PDE-based methods:** Perona-Malik, Total Variation
- **Deep learning:** ColorDnCNN, Fourier Neural Operator (FNO)

## Key findings

- FNO best preserved colour grade across all five LUTs under standard PSNR/SSIM evaluation.
- A domain-adapted DnCNN (retrained on graded image patches) surpassed FNO 
  once retrained on graded data — isolating **domain mismatch**, not 
  architecture, as the root cause of standard CNN underperformance.
- Methods with strong pixel-fidelity scores (PSNR/SSIM) can actively worsen 
  colour fidelity in graded images — a gap invisible to standard metrics.

## Stack

Python · PyTorch · NumPy · scikit-image

## Author

Prerna Mehra — B.Sc. Mathematics & Physics, GPGC Ranikhet
