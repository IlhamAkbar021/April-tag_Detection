<div align="center">

# 🎯 April Tag Accuracy & Repeatability Tool

**A visual benchmarking and evaluation tool for analyzing approach trajectories, accuracy, and repeatability across different robotic navigation methods.**

[![ROS](https://img.shields.io/badge/ROS-Noetic-22314E?style=for-the-badge&logo=ros)](#)
[![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)](#)
[![OpenCV](https://img.shields.io/badge/OpenCV-Computer_Vision-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)](#)

<img width="777" height="413" alt="Screenshot from 2026-09-07 11-43-21" src="https://github.com/user-attachments/assets/abca4a52-7d47-4c5a-a720-7a56eb81f966" />

</div>

---

> **Overview for Product Performance Teams**  
> Designed as a lightweight visual tool to benchmark and compare different robot navigation algorithms. Rather than replacing high-precision reference sensors (such or lasers-Jig), it provides a fast, empirical reference to evaluate final approach positioning and verify that alternative navigation strategies achieve consistent, millimeter-level accuracy.

## 🎛️ Evaluation & Testing Controls
*   **Live Matrices:** Real-time display of Tag ID, Distance (m), X/Y offsets (m), and Heading angle (degrees) relative to the head camera lens.
*   **Record:** Logs instant pose metrics into the session table to sample positional accuracy.
*   **Register (Zeroing):** Sets the tag's initial pose as the reference baseline. Allows teams to measure relative positioning errors during approach initialization without being affected by physical tag tilt or offset.
*   **Unregister:** Resets the active zero baseline back to raw camera frame coordinates for uncompensated testing.
*   **Headless Mode:** Disables video stream rendering to save memory and CPU cycles, ensuring the benchmark tool itself does not interfere with the robot's onboard navigation performance.

## 📊 Data Management & Reporting

*   **Metrics Table:** Interactive data logging grid that converts distance and lateral offsets to centimeters for straightforward error analysis.
*   **Export Data:** Saves benchmark sessions directly to `.csv` format for statistical comparison, standard deviation calculations, and cross-approach error analysis.
*   **Data Scrubbing:** Allows quick deletion of invalid or interrupted trial runs to keep evaluation datasets clean.

---

<details>
<summary><b>📦 System Dependencies (Click to Expand)</b></summary>
<br>

Ensure the following packages are installed in your environment:
*   `ros-noetic-desktop`
*   `python3`
*   `opencv-python` (with ArUco/AprilTag module)
*   `cv_bridge`
*   `PyQt5`
*   `numpy`
*   `tf` / `tf.transformations`

</details>

---

## 🚀 Quick Start

Ensure ROS core is active and your camera topic is publishing, then run the script directly:

```bash
# Enter to inside-docker
cd ~/aeolus; bin/dr enter

# Navigate to workspace source directory
cd /var/aeolus/data_ws/src

# Launch the tool directly via Python
python april_tag.py
