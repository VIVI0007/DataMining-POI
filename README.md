# POI-Based Predictive Modeling for EV Charging Station Analysis

This project implements a suite of baseline machine learning models for evaluating the spatial prediction of Points of Interest (POIs), such as electric vehicle charging stations. The models include Geographically Weighted Regression (GWR), Kriging, Random Forests, and Neural Networks.

---

## 📁 Project Structure


---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/poi-ev-charging-stations.git
cd poi-ev-charging-stations
```

###2. Create Virtual Environment
Create a virtual environment to manage dependencies:

```bash
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
```
##3. Install Dependencies
Install the necessary libraries by running:

```bash
pip install -r requirements.txt
⚠️ Ensure that you're using tensorflow==1.15 to ensure compatibility with keras==2.1.5.
```
##🧠 Models Included
###The following models are included in this repository:

Geographically Weighted Regression (GWR): A spatial regression model that takes into account the geographical location of each observation.

Linear Kriging: Combines linear regression for the mean model and Gaussian Process regression for the spatial residuals.

Random Forest Kriging: A variant of Kriging that uses Random Forests as the regression model for the mean.

Neural Network: A deep learning model with multiple layers of perceptrons using tf.keras.

##🧪 Running Baseline Models
You can run all baseline experiments using the main.py script:

```bash
python main.py
```
The script will:

Load and process the data using the project-specific data pipeline.

Train each model (GWR, Kriging, Random Forest, Neural Network).

Save results such as evaluation metrics, model settings, and performance statistics into the output/ folder.

##📊 Output
Each model run generates a JSON file containing the model's evaluation metrics, training time, and predictions. The output is saved in the following structure:

text
output/
└── <project-name>/
    └── <model-name>/
        └── information.json
Example information.json
The information.json file includes:

Model configuration and hyperparameters

Training time and prediction latency

In-sample and out-of-sample predictions

Evaluation metrics (e.g., Mean Squared Error)

##📦 Dependencies
The project relies on the following key libraries:

tensorflow==1.15

keras==2.1.5

scikit-learn

mgwr

loguru

pandas

numpy

matplotlib

seaborn

You can install them manually by running:

```bash
pip install tensorflow==1.15 keras==2.1.5 scikit-learn mgwr loguru
📁 Project Structure
text
poi-ev-charging-stations/  
│  
├── poi/  
│   ├── baselines.py # Core ML model pipeline definitions  
│   ├── helpers.py # Utility functions: JSON saving, model naming, etc.  
│   ├── paths.py # File path utilities for output saving  
│   └── ...  
├── data/ # Input datasets  
├── output/ # Model outputs (automatically created)  
├── main.py # Main script to launch experiments  
└── README.md # This file  
```
