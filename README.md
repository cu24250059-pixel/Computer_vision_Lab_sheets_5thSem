# Computer Vision Lab Sheets (5th Semester)

Repository containing practical lab sheets, implementations, and experiments for the **Computer Vision Lab** course (5th Semester, B.Tech CSE).

---

## 👨‍🎓 Student & Course Details

| Detail | Information |
| :--- | :--- |
| **Student Name** | Abhigyan Dubey |
| **Course & Branch** | B.Tech Computer Science & Engineering |
| **CUID / Roll No.** | `CU24250059` |
| **Subject** | Computer Vision Lab |
| **Semester & Section** | 5th Semester, Section "B" |

---

## 📚 Experiments Index

### 🔬 [Experiment 1: Fundamental Image Processing Operations](experiment_1.ipynb)
An in-depth introduction to core digital image processing operations, representation of images as multi-dimensional NumPy arrays, color space conversions, and geometric transformations.

#### Breakdown of Steps Covered in Experiment 1:
1. **Library Imports & Setup:**
   * `cv2` (OpenCV): Core image reading, writing, filtering, transformations, and color conversions.
   * `numpy`: Efficient multi-dimensional array operations on pixel matrices.
   * `matplotlib.pyplot`: In-notebook visualization, plotting, and multi-panel image comparisons.
   * `os` / `pathlib`: Cross-platform file path management and output directory generation.

2. **Image Ingestion & Display:**
   * Reading images from disk using `cv2.imread()`.
   * Handling OpenCV's default **BGR** color space vs. Matplotlib's standard **RGB** format using `cv2.cvtColor(img, cv2.COLOR_BGR2RGB)` to prevent channel swapping artifacts.

3. **Image Attributes & Metadata Inspection:**
   * Checking dimensions (`height, width, channels`) via `.shape`.
   * Inspecting pixel data types (`uint8` with value ranges `[0, 255]`) via `.dtype`.

4. **File Formats & Compression Comparison:**
   * Saving images using `cv2.imwrite()`.
   * Evaluating trade-offs between **JPEG** (lossy compression, smaller size) and **PNG** (lossless compression, preserves transparency and exact pixel values).

5. **Color Space Transformations:**
   * **Grayscale (`BGR2GRAY`):** Single-channel intensity representation for efficient computation.
   * **HSV (`BGR2HSV`):** Hue, Saturation, Value separation for lighting-invariant color thresholding and object tracking.
   * **CIELAB (`BGR2LAB`):** Perceptually uniform color representation separating Lightness ($L^*$) from chromatic axes ($a^*$, $b^*$).

6. **Geometric Transformations:**
   * **Scaling / Resizing:** Dimension adjustments using `cv2.resize()`.
   * **Rotation:** Center-point affine transformations via `cv2.getRotationMatrix2D()` and `cv2.warpAffine()`.
   * **Flipping:** Horizontal mirror (`1`), vertical mirror (`0`), and dual-axis inversion (`-1`) via `cv2.flip()`.

7. **Image Complement (Negative):**
   * Pixel intensity inversion via vectorized NumPy array subtraction (`255 - image`).

8. **Region of Interest (ROI) Extraction:**
   * Spatial sub-array slicing using standard NumPy array coordinates `img[y_start:y_end, x_start:x_end]`.

9. **Output Export:**
   * Automated export of all processed image variants to a local `outputs/` directory.

---

## 🛠️ Prerequisites & Installation

To run the lab notebooks locally or in Jupyter, install the required dependencies:

```bash
# Clone the repository
git clone https://github.com/cu24250059-pixel/Computer_vision_Lab_sheets_5thSem.git
cd Computer_vision_Lab_sheets_5thSem

# Install required Python packages
pip install opencv-python numpy matplotlib notebook
```

---

## 🚀 How to Run

1. Launch Jupyter Notebook or JupyterLab:
   ```bash
   jupyter notebook
   ```
2. Open [`experiment_1.ipynb`](experiment_1.ipynb).
3. Set the `IMAGE_PATH` variable in the configuration cell to your target input image.
4. Run all cells sequentially (`Shift + Enter` or `Kernel -> Restart & Run All`).
5. Processed output images will be generated in the `outputs/` directory.

---

## 💡 Key Takeaways

* **OpenCV vs. Matplotlib Color Channels:** OpenCV loads color channels in **BGR** order by default; conversion to **RGB** is necessary prior to rendering with Matplotlib.
* **Vectorized Array Computing:** Images are treated as $H \times W \times C$ NumPy arrays, allowing cropping, arithmetic transformations, and color negation to be performed as fast one-line matrix operations.