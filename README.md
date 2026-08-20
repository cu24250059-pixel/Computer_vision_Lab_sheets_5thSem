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
### 🔬 [Experiment 1: Contrast Enhancement and Histogram-Based Image Processing using Python and OpenCV](Experiment2Solution.ipynb)

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
