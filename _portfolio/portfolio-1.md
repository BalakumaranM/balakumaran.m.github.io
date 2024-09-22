---
title: "Stacking Sequence Optimization of a Laminated Composite C-Section Using Neural Networks"
excerpt: "Short description of portfolio item number 1<br/><img src='/images/mtp portfolio1.png'>"
collection: portfolio
---

## Overview
This project focuses on optimizing the stacking sequence of a laminated composite C-section using **Multi-Criteria Decision Making (MCDM)** and **Neural Networks**. The project involved detailed **structural analysis** of the composite C-section to predict **failure indices**, **buckling load multipliers**, and **deformation values**. I utilized **Classical Laminate Theory (CLT)** and **Finite Element Analysis (FEA)** for initial analysis, followed by **Machine Learning** and **Deep Neural Networks (DNN)** to streamline the design process.

## Structural Analysis
### Initial Design
The C-section was subjected to axial and shear loading, and its structural response was evaluated using **Classical Laminate Theory**. The laminate was composed of **16 plies** with orientations such as \( \pm45^{\circ}, 0^{\circ}, 90^{\circ} \), and the analysis was aimed at minimizing the **failure index** while ensuring structural integrity under various loading conditions.

- **Material**: Hexply M21/T800S carbon-epoxy prepreg
- **Mechanical properties**: Longitudinal modulus \(E_1 = 1.72 \times 10^5 \text{ MPa}\), Transverse modulus \(E_2 = 10000 \text{ MPa}\)
- **Geometric properties**: The laminate was 4 mm thick with a ply thickness of 0.25 mm.
  
### Results from Classical Laminate Theory
The **failure index** for the initial stacking sequence was calculated based on **Tsai-Hill failure criteria**, indicating that shear failure occurs at the highest load.

- Initial stacking sequence: \( \pm45^{\circ}/0^{\circ}/\pm45^{\circ}/90^{\circ}/\pm45^{\circ} \)
- Failure Index (shear): **0.6505**
  
By applying **Generalized Reduced Gradient (GRG)** optimization, the stacking sequence was optimized to reduce the failure index, and the design constraints were met for factors like buckling load and deformation.

*Include an image here illustrating the FEA analysis results (e.g., stress and deformation plots)*.

## AI and Machine Learning Implementation
The major innovation in this project was the use of **machine learning** to predict structural responses for different stacking sequences. Instead of running time-consuming FEA simulations for every possible configuration, I trained a **Deep Neural Network (DNN)** to predict important structural responses such as **Total Deformation**, **Maximum Principle Stress**, and **Failure Index**.

### Data Preparation
Data from 70 different stacking sequences was generated using FEA for various loading cases (e.g., axial, shear, and bending). The input data consisted of stacking sequences and corresponding structural responses such as stress, strain, and deformation values. The dataset was split into training and test sets, and normalization techniques were applied to ensure stable model training.

### Neural Network Architecture
The neural network used for this project had:
- **Input layer**: Representing the stacking sequence and load conditions
- **Hidden layers**: Three fully connected layers to capture nonlinear relationships between input features
- **Output layer**: Predicting **AHP scores**, **failure indices**, and **deformation values**

*Insert a diagram here showing the architecture of the neural network used.*

### Training and Results
The neural network was trained using **backpropagation** with a **mean squared error loss function**. The model successfully predicted the structural responses with an accuracy of 95% within 1.46 seconds for any given stacking sequence, significantly reducing the computational effort required for FEA simulations.

*Add a plot showing training and validation loss over epochs to visualize the network performance.*

### Key Findings
- The neural network could predict failure indices for untested stacking sequences, providing a quick and efficient way to evaluate different designs.
- The model was also fine-tuned to predict results under different weightings of design criteria (e.g., prioritizing deformation over failure index).

You can view the code for this implementation on my [GitHub repository](https://github.com/BalakumaranM/Stress-prediction-using-ann-).

## Conclusion
This project demonstrated the powerful combination of **Classical Laminate Theory** and **Deep Learning** in optimizing composite structures. By using **AI**, the process of analyzing and predicting structural behavior was significantly accelerated, allowing for quicker design iterations.

## Next Steps
Future work could explore the use of **Physics-Informed Neural Networks (PINNs)** to directly integrate physical laws into the neural network model, potentially further improving accuracy and reducing the need for extensive training data.

---

*For additional information, refer to my thesis document and include figures showing the FEA analysis, stress-strain curves, and neural network performance.*
