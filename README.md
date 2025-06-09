# Configuration Identification of On-demand Variable Stiffness Strain-Limiting Layers in Zig-zag Soft Pneumatic Actuators using Deep Learning Methods

## Soft Pneumatic Actuator Configuration Prediction
This repository contains the codebase for the paper "Predicting Modular Strain-Limiting Layer Configurations for Soft Pneumatic Actuators Using Neural Networks". The project presents a novel machine learning-based framework to determine optimal modular strain-limiting layer (SLL) configurations that generate specific tip-point trajectories in soft pneumatic actuators (SPAs) — without the need for structural redesign or re-fabrication.

## Overview
Traditional SPAs produce fixed trajectories based on their structural design, limiting their flexibility across applications. This work overcomes that limitation by:

1. Enabling multiple trajectories from a single SPA structure
2. Predicting SLL configurations using:
   a. A feed-forward neural network (FNN) approach.
   b. A convolutional neural network (CNN)-based architecture.
   
The models learn the inverse mapping from desired Cartesian tip trajectories to SLL configurations, enabling function-specific and application-adaptive soft robotic systems.

## Features
1. ML-based inverse design of SPAs.
2. Generalizable to various SPA applications.
3. Supports configurations for:
  a. Endoscope-style motion.
  b. Soft robotic gripping.
  c. Bio-inspired finger actuation.


## 🚀 Getting Started with Google Colab

1. **Access Colab**  
   Visit [colab.research.google.com](https://colab.research.google.com).

2. **Create a Notebook**  
   Click on **"New Notebook"** or open an existing `.ipynb` file.

3. **Write Code**  
   Add Python code in code cells and use text cells (Markdown) for documentation.

4. **Run Code**  
   Click the **"Run"** button or press `Shift + Enter`.

5. **Save and Share**  
   Save to Google Drive or download as `.ipynb` or `.py`. Easily share with others via link.

6. **Install Libraries**  
   Use `!pip install` for installing additional libraries.

7. **Use GPU/TPU**  
   Navigate to **Runtime > Change runtime type** and select **GPU** or **TPU** for better performance.

---

## 📦 Installation

Google Colab comes with most of the necessary Python libraries pre-installed. In most cases, you won't need to install anything additional.

---

## 📁 Project Structure

All project notebooks are located in the `Codes/` directory. The folder includes:

- `FNN/` - Feedforward Neural Network Notebooks
- `CNN/` - Convolutional Neural Network Notebooks
- `Polynomial Regression/` - Polynomial Regression Model
- `Calculate_Finger_Results.ipynb`
- `Different_Number_of_Parameters.ipynb`

---

## 📂 Detailed Contents

### 🔹 FNN - Feedforward Neural Networks

Located in `Codes/FNN/`

#### `With Experimental Data.ipynb`
- Requires:
  - `5_Randomly_Selected_Configurations.csv`
  - `Interpolated_Training_Data.csv`
  - `Predicted_Thetas.csv`
  - `Predicted_Thetas_Fingers.csv`
- Location: `For Paper/FNN/With Experimental Data/`

#### `With Simulation Data.ipynb`
- Requires:
  - `5_Randomly_Selected_Configurations.csv`
  - `Simulation_Training_Data.csv`
  - `Predicted_Thetas.csv`
- Location: `For Paper/FNN/With Simulation Data/`

---

### 🔹 CNN - Convolutional Neural Networks

Located in `Codes/CNN/`

#### `Trajectories with CNN-Experiment.ipynb`
- Requires image folders:
  - `Arbitrary Trajectory Pictures`
  - `Equation Trajectory Pictures`
  - `Increasement Picture`
  - `Real Trajectory Pictures`
  - `Finger Trajactory Images`
- Location: `For Paper/CNN/Experiment/`

#### `Trajectories with CNN-Simulation.ipynb`
- Requires image folders:
  - `Arbitrary Trajectory Pictures`
  - `Equation Trajectory Pictures`
  - `Increasement Picture`
  - `Real Trajectory Pictures`
- Location: `For Paper/CNN/Simulation/`

---

### 🔹 Polynomial Regression

Located in `Codes/Polynomial Regression/`

#### `Get Theta 1-5 by Theta 6 (Poly Regression).ipynb`
- Requires: `Interpolated_Training_Data.csv`
- Location: `For Paper/Polynomial Regression/`

---

### 🔹 Different Number of Parameters

#### `Different Number of Parameters.ipynb`
- Evaluates optimal parameter count for the project
- Requires: `Interpolated_Training_Data.csv`
- Location: `For Paper/Different Number of Parameters/`

---

### 🔹 Calculate Finger Results

#### `Calculate_Finger_Results.ipynb`
- Calculates R-squared, MSE, RMSE, and MAE metrics
- Compares predicted trajectories with actual results
- Requires:
  - `fingerVSConfig_for_CNN`
  - `fingerVSConfig_for_DNN`
- Location: `For Paper/Calculate_Finger_Results/`

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to modify.

Make sure to update relevant tests as needed.

---

## 🗨️ Correspondance 
Hiroshan Gunawardane - hiroshan@mail.ubc.ca 
Duhyeon Lee - duhyeon@student.ubc.ca

---

## 📄 License

MIT License

```
MIT License

Copyright (c) 2025 Hiroshan Gunawardane

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
