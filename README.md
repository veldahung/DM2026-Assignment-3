# DM2026-Assignment-3

### 🚨 IMPORTANT NOTICE: WHICH FILE TO EVALUATE 🚨
Please ensure you download and run **`DM_HW3_complete.ipynb`**.

* **✅ USE:** **`DM_HW3_complete.ipynb`** — This file contains all the methods applied in the Kaggle competition, including the first-try method outputs. You MUST use this file to get the exact results matching the report and the Kaggle leaderboard.
* **❌ DO NOT USE:** `DM_HW3_rerun.ipynb` — This file is provided *only* as a supplementary record of the re-run outputs mentioned in the report.

## How to Run the Code (Recommended: Google Colab)

> ⚠️ **CRITICAL:** You must use **`DM_HW3_complete.ipynb`** to evaluate this assignment and reproduce the final report results. Do not run the `DM_HW3_rerun.ipynb` file for the main evaluation.

The code is optimized to run on Google Colab to utilize cloud GPUs and avoid local environment setup issues.

**Step-by-Step Instructions:**

1. **Download the Notebook:** Download the file named `DM_HW3_complete.ipynb` (the "complete" file) to your local machine.
2. **Open Google Colab:** Navigate to [Google Colab](https://colab.research.google.com/) and upload the `DM_HW3_complete.ipynb` file.
3. **Select the T4 GPU:**
* In the Colab top menu, go to **Runtime** > **Change runtime type**.
* Under "Hardware accelerator", select **T4 GPU** and save.


4. **Prepare Kaggle API Credentials:**
* Log in to your Kaggle account, go to your Account Settings, and click "Create New API Token" to download your `kaggle.json` file.
* Make sure you have accepted the rules for the `nycu-data-mining-assignment-3` competition on Kaggle.


5. **Run the Notebook:**
* Execute the first code cell.
* It will prompt you to **upload the `kaggle.json` file**. Click "Choose Files" and upload the file you downloaded in step 4.
* Run the subsequent cells. The notebook will automatically configure the Kaggle credentials, download the competition dataset, extract it, and begin the data loading and training process.



---

## Other Possible Methods to Run the Code

### Method A: Kaggle Kernels (Cloud)

If you do not want to use Colab, you can run the code directly on Kaggle's servers.

1. Go to the `nycu-data-mining-assignment-3` Kaggle competition page and click **New Notebook**.
2. Go to **File > Import Notebook** and upload `DM_HW3_complete.ipynb`.
3. In the notebook settings on the right-hand panel, ensure the **Accelerator** is set to **GPU T4x2**.
4. **Code Adjustments:** Because Kaggle already has the data mounted, you must comment out or delete the cells that install the Kaggle API, upload `kaggle.json`, and download/unzip the data. You will also need to update `TRAIN_DIR` and `TEST_DIR` to point to Kaggle's default `../input/...` directory.

### Method B: Local Jupyter Environment

You can run this on your own machine if you have a capable GPU and sufficient RAM.

1. Ensure you have Python 3.8+ installed.
2. Install the required dependencies in your terminal:
```bash
pip install tensorflow pandas numpy scikit-learn matplotlib seaborn tqdm lightgbm xgboost kaggle

```


3. Place your `kaggle.json` file in the `~/.kaggle/` directory (Mac/Linux) or `C:\Users\<Your-Username>\.kaggle\` (Windows).
4. Launch Jupyter:
```bash
jupyter notebook DM_HW3_complete.ipynb

```


5. **Code Adjustments:** You will need to comment out the Google Colab specific cell (`from google.colab import files; files.upload()`). The Kaggle API will automatically use the `.kaggle/kaggle.json` file on your system to download the data.
