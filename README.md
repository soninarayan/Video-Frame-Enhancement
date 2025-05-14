# Spline Interpolation for Frame Rate Enhancement

## Project Overview
This project uses **cubic spline interpolation** to boost video frame rates, improving smoothness and visual fidelity.

---

## Environment Setup

### Prerequisites
-   **Python** 3.8+
-   **pip** package manager
-   **macOS** on Apple Silicon (M1/M2)

### Installation
1.  Clone or download the repo.
2.  In the project root, install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

    ⸻

    requirements.txt

    ```
    numpy==1.26.4
    scipy==1.13.0
    opencv-python==4.9.0.80
    matplotlib==3.8.4
    ```

    ⸻

    Dataset
    * Source: Any YouTube video
    * Original FPS: 30
    * Downsampled FPS: 10
    * Clip Length: 15 seconds

    ⸻

    Preparing the Dataset
    1.  Download your YouTube video.
    2.  Downsample to 10 FPS (e.g., using ffmpeg):

        ```bash
        ffmpeg -i input.mp4 -r 10 downsampled_input.mp4
        ```

    3.  Trim to 15 seconds:

        ```bash
        ffmpeg -i downsampled_input.mp4 -t 15 trimmed_input.mp4
        ```

    4.  Place trimmed\_input.mp4 in the project root (or update the path in main.py).

    ⸻

    File Structure

    ```
    .
    ├── README.md
    ├── ground_truth.mp4       # Original 30 FPS clip
    ├── input.mp4             # 10 FPS source clip
    ├── main.py               # Spline interpolation script
    ├── output_video.mp4      # 30 FPS result via cubic spline
    ├── output2_video.mp4     # Alternative interpolation variant
    └── requirements.txt
    ```

    ⸻

    Usage

    From the project root:

    ```bash
    python3 main.py
    ```

    * Output:
        * output\_video.mp4 — primary 30 FPS result
        * output2\_video.mp4 — secondary/intermediate variant (see comments in main.py for details)

    ⸻

    Viewing Results

    Open any video player (e.g., VLC, QuickTime) and compare:
    * ground\_truth.mp4 (30 FPS original)
    * input.mp4 (10 FPS downsampled)
    * output\_video.mp4 (spline‐interpolated)
    * output2\_video.mp4 (variant output)

    Enjoy smoother motion and feel free to tweak spline parameters in main.py!
