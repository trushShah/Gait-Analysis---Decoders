# Multivariate Gait Data Analysis: A Micro and Macro Level Study

## Abstract
This project presents a comprehensive analysis of human gait biomechanics using the *Multivariate Gait Data* from the UCI Machine Learning Repository. The study explores both micro-level (time-series) and macro-level (cycle-wise aggregated) gait characteristics of healthy individuals under normal (unbraced) and motion-restricted (braced) conditions.  
By applying statistical feature extraction, anomaly detection, and classification methods, the study aims to quantify gait variability, identify deviations in movement patterns, and evaluate the overall gait health of subjects.

---

## Project Objectives
1. To investigate gait behavior at micro (time-series) and macro (aggregated) levels.  
2. To extract kinematic features such as joint angle, velocity, and acceleration across gait cycles.  
3. To detect gait anomalies using unsupervised models such as Isolation Forest and One-Class SVM.  
4. To classify gait condition (unbraced vs braced) using supervised models like Logistic Regression and Random Forest.  
5. To summarize gait health through a combined anomaly and classification-based gait score.

---

## Dataset Description

- **Source:** UCI Machine Learning Repository – *Multivariate Gait Data*  
- **Subjects:** 10 healthy individuals  
- **Conditions:**
  - **Condition 1:** Unbraced (normal walking)
  - **Condition 2 and 3:** Braced (restricted walking)
- **Data Type:** Multivariate time-series of lower-limb joint angles captured during gait cycles.

### Columns and Features

| Column | Description |
|---------|--------------|
| `subject` | Identifier for each participant (1–10) |
| `condition` | Walking condition (1 = unbraced, 2/3 = braced) |
| `replication` | Trial number per subject |
| `angle_mean` | Mean joint angle (degrees) over a gait cycle |
| `angle_std` | Standard deviation of joint angle |
| `angle_min`, `angle_max`, `angle_median` | Minimum, maximum, and median joint angle |
| `vel_mean`, `vel_std`, `vel_min`, `vel_max`, `vel_median` | Velocity statistics (first derivative of angle) |
| `acc_mean`, `acc_std`, `acc_min`, `acc_max`, `acc_median` | Acceleration statistics (second derivative of angle) |
| `condition_binary` | Encoded binary label (0 = unbraced, 1 = braced) |

---

## Project Structure

This project is divided into two major parts:

### 1. **Micro-Level Analysis**
- Focuses on the raw time-series gait signals of each subject.  
- Computes joint angle, velocity, and acceleration profiles.  
- Explores gait cycle consistency and variation under braced vs unbraced conditions.  
- Outputs: aggregated feature summaries per gait cycle for macro analysis.

### 2. **Macro-Level Analysis**
- Uses cycle-wise aggregated data for machine learning.  
- **Anomaly Detection:** Isolation Forest, One-Class SVM trained on unbraced data.  
- **Classification:** Logistic Regression and Random Forest to distinguish gait conditions.  
- Evaluates feature importance and develops a combined gait health score.

---

## Files in This Repository

| File | Description |
|------|--------------|
| `Micro_Level_Analysis.ipynb` | Preprocessing and feature extraction from raw time-series gait data. Computes velocity, acceleration, and visualizes joint motion patterns. |
| `Macro_Level_Analysis.ipynb` | Performs anomaly detection and classification on aggregated gait cycles. Includes model evaluation and gait score computation. |
| `README.md` | Project documentation outlining objectives, dataset, and methodology. |

---

**Dataset Reference:**  
> Helwig, N. & Hsiao-Wecksler, E. (2016). Multivariate Gait Data [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5861T.
> https://archive.ics.uci.edu/dataset/760/multivariate+gait+data

---


