# Influence-Score-Based-Trajectory-prediction-of-Autonomous-Vehicles-using-LSTM-and-GNN-
Source code for Research paper

Trajectory Prediction with Influence Score
This project demonstrates a trajectory prediction model using LSTM networks with and without influence scores. It explores how incorporating influence scores can improve the accuracy and reliability of trajectory prediction, especially in contexts where additional contextual or external factors impact motion or path planning (e.g., autonomous vehicles, robotic navigation, or human movement prediction).

Table of Contents \n
Overview \n
Research Motivation and Benefits \n
Dataset and Preprocessing \n
Model Architecture\n
Training and Evaluation\n
Results and Comparisons\n
Getting Started\n
Future Work\n
Acknowledgments\n
Overview
Trajectory prediction is essential in various fields, from autonomous navigation to sports analytics. This project introduces a method for enhancing trajectory prediction by integrating influence scores — contextual factors or additional data points that may impact the trajectory. The system demonstrates:

A standard LSTM model for trajectory prediction.
An LSTM model that incorporates an influence score as an additional feature to improve prediction accuracy.
Research Motivation and Benefits
Incorporating influence scores enables more realistic and precise predictions by including external or contextual factors that impact trajectories. This approach can benefit:

Autonomous Vehicles: More accurate predictions of pedestrian and vehicle paths by considering external factors.
Robotic Navigation: Enhanced path planning by integrating environmental influence scores.
Human Movement Prediction: Improved predictions of movement patterns in health or sports applications.
Dataset and Preprocessing
Synthetic data is generated for demonstration purposes, consisting of:

Trajectory Data: Each sample is a 10-step sequence with (x, y) coordinates.
Influence Score: A single numerical value representing external influence (e.g., environmental factors).
The data is organized in a format compatible with PyTorch's Dataset and DataLoader classes to facilitate model training.

Model Architecture
Two models are implemented using PyTorch:

Trajectory LSTM without Influence Score:
Input: Trajectory sequence (x, y) coordinates.
Structure: LSTM layer followed by a fully connected layer to predict the next position.
Trajectory LSTM with Influence Score:
Input: Trajectory sequence (x, y) coordinates plus an influence score.
Structure: Influence score is concatenated as an additional feature in each timestep, passed through the LSTM and fully connected layer.
Training and Evaluation
The training process involves:

Loss Calculation: Mean Squared Error (MSE) between predicted and actual trajectory positions.
Metrics: Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE) for performance evaluation.
During training, the model with influence scores is compared to the baseline model to assess improvement in trajectory prediction accuracy.

Results and Comparisons
After training, we plot and compare:

Training Loss Over Epochs: Shows how each model learns over time.
Performance Metrics (MAE & RMSE): Highlights the predictive accuracy of each model, indicating the advantage of using influence scores.
Example Plots
Training Loss Plot: Shows the loss trends over epochs for both models.
Metric Comparison: Bar plot comparing MAE and RMSE for both models, highlighting the influence score's effect.
Getting Started
Prerequisites
Python 3.x
PyTorch, NumPy, Matplotlib
Installation
Clone this repository and install the required dependencies:

bash
Copy code
git clone https://github.com/ArnavJain42/Influence-Score-Based-Trajectory-prediction-of-Autonomous-Vehicles-using-LSTM-and-GNN-
cd Influence-Score-Based-Trajectory-prediction-of-Autonomous-Vehicles-using-LSTM-and-GNN-
Run the Jupyter Notebook file (Trajectory_Prediction.ipynb) to train and evaluate the models:
and install dependencies

bash
Copy code
jupyter notebook Trajectory_Prediction.ipynb
Future Work
Potential enhancements include:

Testing on real-world trajectory datasets.
Incorporating multiple influence scores or additional contextual data.
Extending to more complex trajectory models or sequences with variable lengths.
Acknowledgments
This research was conducted to explore trajectory prediction improvements using influence scores, with potential applications in autonomous systems and robotics. Special thanks to collaborators and resources that inspired the synthetic data generation and modeling techniques.
