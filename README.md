# Lab 1: Image as a 2D Signal

This lab explores how digital images can be treated as two-dimensional (2D) signals.  
We focus on key image processing operations such as **quantization**, **histogram analysis**, **contrast stretching**, **gamma correction**, and **sampling**.

---

## 1. Original and Grayscale Image

### 🔹 Explanation
An image can be represented as a 2D matrix of intensity values.  
Color images (RGB) have three channels, while grayscale images have one channel representing brightness.  
Converting to grayscale simplifies analysis since we only deal with intensity information.


## 🎚️ 2. Quantization and Dynamic Range

### 🔹 Explanation
Quantization refers to reducing the number of possible intensity levels (bit depth).  
- **8-bit image:** 256 gray levels (smooth transitions).  
- **6-bit image:** 64 gray levels.  
- **4-bit image:** 16 gray levels (visible banding or posterization).

Reducing bit depth increases visual artifacts because fewer intensity levels are available to represent smooth variations.


## 📊 3. Histogram and Contrast Stretching

### 🔹 Explanation
The histogram shows how pixel intensities are distributed.  
- A narrow histogram means low contrast (most pixels have similar brightness).  
- Contrast stretching **expands** this range, making dark areas darker and bright areas brighter.

In MATLAB, `imadjust` or `mat2gray` can be used for stretching.  
This enhances visibility and detail in both light and dark regions.


## ⚡ 4. Gamma Correction (Nonlinear Brightness Adjustment)

### 🔹 Explanation
Gamma correction adjusts image brightness **nonlinearly**:
- **Gamma < 1:** brightens the image (useful for dark images).  
- **Gamma > 1:** darkens the image (useful for overexposed images).  

Unlike contrast stretching (linear mapping), gamma correction affects midtones more strongly and changes how humans **perceive** brightness.


## 🔻 5. Sampling and Aliasing

### 🔹 Explanation
Sampling reduces the spatial resolution of an image.  
If we downsample an image too much, fine details are lost.  
When the image is later upsampled back, the lost details cannot be recovered, and **aliasing artifacts** (like jagged edges or repeating patterns) appear.

This happens because of the **Nyquist theorem**, which states that the sampling frequency must be at least twice the highest frequency of the signal to avoid aliasing.



## 💭 6. Reflections and Learning Outcomes

### 🔹 Key Observations
1. **Bit-depth reduction (Quantization)** caused visible banding — fewer gray levels made smooth areas appear blocky.  
2. **Contrast Stretching** expanded intensity range, improving clarity and revealing hidden details.  
3. **Gamma Correction** changed perceived brightness nonlinearly — effective for display adjustments.  
4. **Sampling and Aliasing** showed how aggressive downsampling can distort visual information and cause loss of details.

### 🧠 Key Learning Points
- Images are 2D signals defined over discrete pixels.  
- Quantization and sampling both limit the fidelity of digital images.  
- Proper enhancement techniques (stretching, gamma correction) can significantly improve image visibility and quality.


## 🧰 Tools Used
- **MATLAB Online**
- Built-in functions: `imread`, `imshow`, `rgb2gray`, `mat2gray`, `imadjust`, `imhist`, `imresize`, `montage`



**Prepared by:** *Rupashri Das*  
**Date:** 29 October 2025  
**Course:** Mathematical Algorithms

---
