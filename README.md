# Technical Report: Edge Detection

**Instructor**: Olivier Laligant  
**Author**: Mayank Kumar GUPTA  

---

## Summary

This experiment uses edge detectors like Prewitt, Sobel, Scharr, and pure derivatives. An image with a vertical edge at the center is generated, Gaussian white noise is added, and Signal-to-Noise Ratio (SNR) is calculated. The F-score for each edge detector is computed at various thresholds.

---

### Steps

#### 1. Vertical Edge Image Generation

An image with a vertical edge at the center is generated. The left half is black (0), and the right half is white (1).

<p align="center"><img src="https://raw.githubusercontent.com/Mayankgbrc/Edge-Detection/refs/heads/main/pdf_images/0.png" alt="Vertical Edge Image" width="400px">
</p>

#### 2. Histogram of the Vertical Edge Image

A histogram of the gray values in the generated vertical edge image is plotted.

<p align="center"><img src="https://raw.githubusercontent.com/Mayankgbrc/Edge-Detection/refs/heads/main/pdf_images/15.png" alt="Histogram of Vertical Edge Image" height="400px">
</p>

#### 3. Adding Gaussian White Noise

Gaussian white noise with mean 0 and standard deviation 0.1 is added to the image.

<p align="center"><img src="https://raw.githubusercontent.com/Mayankgbrc/Edge-Detection/refs/heads/main/pdf_images/1.png" alt="Image with Gaussian Noise" width="400px">
</p>

#### 4. Histogram of Gaussian White Noise

A histogram of the gray values in the Gaussian noise is plotted.

<p align="center"><img src="https://raw.githubusercontent.com/Mayankgbrc/Edge-Detection/refs/heads/main/pdf_images/14.png" alt="Histogram of Gaussian Noise" width="400px">
</p>

#### 5. Noisy Image (Edge + Noise)

The generated vertical edge image with Gaussian noise is displayed.

<p align="center"><img src="https://raw.githubusercontent.com/Mayankgbrc/Edge-Detection/refs/heads/main/pdf_images/2.png" alt="Noisy Edge Image" width="400px">
</p>

#### 6. Histogram of Noisy Image

A histogram of the noisy image (edge + noise) is plotted.

<p align="center"><img src="https://raw.githubusercontent.com/Mayankgbrc/Edge-Detection/refs/heads/main/pdf_images/3.png" alt="Histogram of Noisy Image" width="400px">
</p>

#### 7. Output of Noisy Image with Filters

The noisy image is processed through four edge detectors: **1D Kernel**, **Prewitt**, **Sobel**, and **Scharr**. The results are shown below:

- **1D Kernel Filter (X) and (Y)**
<p align="center"><img src="https://raw.githubusercontent.com/Mayankgbrc/Edge-Detection/refs/heads/main/pdf_images/4.png" alt="1D Kernel Filter X and Y Output" width="500px" />
</p>


- **Prewitt Filter (X) and (Y)**  
  <p align="center"><img src="https://raw.githubusercontent.com/Mayankgbrc/Edge-Detection/refs/heads/main/pdf_images/5.png" alt="Prewitt X and Y Filter Output" width="500px" />
	</p>


- **Sobel Filter (X) and (Y)**  
  <p align="center"><img src="https://raw.githubusercontent.com/Mayankgbrc/Edge-Detection/refs/heads/main/pdf_images/6.png" alt="Sobel X and Y Filter Output" width="500px" />
	</p>


- **Scharr Filter (X) and (Y)**  
<p align="center"><img src="https://raw.githubusercontent.com/Mayankgbrc/Edge-Detection/refs/heads/main/pdf_images/7.png" alt="Scharr X and Y Filter Output" width="500px">
	</p>


#### 8. Suppressed Image and Histogram After Non-Maximum Suppression

The filtered images are processed through non-maximum suppression to suppress weak edges.

- **1D Kernel Filter (X) and (Y)**
<p align="center"><img src="https://raw.githubusercontent.com/Mayankgbrc/Edge-Detection/refs/heads/main/pdf_images/8.png" alt="Suppressed Image After Non-Maximum Suppression" width="500px" />
</p>

- **Prewitt Filter (X) and (Y)**
<p align="center"><img src="https://raw.githubusercontent.com/Mayankgbrc/Edge-Detection/refs/heads/main/pdf_images/9.png" alt="Suppressed Image After Non-Maximum Suppression" width="500px" />
</p>

- **Sobel Filter (X) and (Y)**
<p align="center"><img src="https://raw.githubusercontent.com/Mayankgbrc/Edge-Detection/refs/heads/main/pdf_images/10.png" alt="Suppressed Image After Non-Maximum Suppression" width="500px" />
</p>

- **Scharr Filter (X) and (Y)**
<p align="center"><img src="https://raw.githubusercontent.com/Mayankgbrc/Edge-Detection/refs/heads/main/pdf_images/11.png" alt="Suppressed Image After Non-Maximum Suppression" width="500px" />
</p>

#### 9. SNR Calculation

Signal-to-Noise Ratio (SNR) is calculated as follows:
- **SNR** = (max_image - min_image) / std_noise 
- **SNR_dB** = 20 * log10(SNR)

**SNR**: 17.65  
**SNR (dB)**: 24.94

#### 10. F-Score vs Threshold Plot

The F-Score for each filter is plotted with respect to varying thresholds.

<p align="center"><img src="https://raw.githubusercontent.com/Mayankgbrc/Edge-Detection/refs/heads/main/pdf_images/12.png" alt="F-Score vs Threshold Plot" width="500px">
</p>

#### 11. SNR vs F-Score Plot

The F-Score for each filter is plotted against the SNR values.

<p align="center"><img src="https://raw.githubusercontent.com/Mayankgbrc/Edge-Detection/refs/heads/main/pdf_images/16.png" alt="SNR vs F-Score Plot" width="500px">
</p>

---

### Conclusion

The experiment shows the effectiveness of different edge detectors under varying noise levels and threshold settings. The Scharr filter demonstrated superior performance across higher thresholds, while the Prewitt and Sobel filters performed similarly with consistent F-scores.

---

