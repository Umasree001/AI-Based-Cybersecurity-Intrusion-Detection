# 🛡️ AI-Based Cybersecurity Intrusion Detection & Threat Prediction System

An AI-powered cybersecurity system that analyzes network traffic and classifies it as normal or potentially malicious using Machine Learning. The project includes a Streamlit dashboard with Live Monitoring and Demo Mode.

## 📌 Project Overview

Modern networks generate huge volumes of traffic, making it difficult to identify cyberattacks manually. This project uses a Random Forest classifier to analyze network-flow features and identify suspicious traffic patterns.

## 🎯 Objectives

- Detect normal and malicious network traffic.
- Classify traffic into multiple attack categories.
- Display predictions and confidence scores in a Streamlit dashboard.
- Provide Live Monitoring and Demo Mode for demonstration and testing.

## 🧰 Technologies Used

- **Language:** Python
- **Machine Learning:** Scikit-learn, Random Forest Classifier
- **Data Processing:** Pandas, NumPy
- **Dashboard:** Streamlit
- **Network Monitoring:** Scapy
- **Dataset:** CICIDS2017

## 🗂️ Dataset

The system uses the CICIDS2017 intrusion detection dataset, which contains benign traffic and multiple categories of network attacks.

The model is configured to work with 78 network-flow features and 15 traffic classes.

Attack categories include:

- DoS and DDoS
- Brute Force
- Port Scan
- Botnet
- Web Attacks
- Infiltration
- Heartbleed
- Benign (normal traffic)

## ⚙️ System Architecture

- **Live Mode:** Captures network packets and processes traffic through the feature extraction pipeline.
- **Demo Mode:** Uses sample network-flow records for demonstrations and testing.
- **Feature Processing:** Prepares input features for the trained model.
- **Random Forest Model:** Predicts the traffic class.
- **Streamlit Dashboard:** Displays predictions, metrics, charts, and activity information.

Live detection depends on the correct implementation of packet capture and feature extraction.

## 📊 Model

The project uses a Random Forest Classifier for multiclass network-traffic classification.

The reported accuracy during development was 98.64% on the evaluated dataset split. Actual performance may vary, particularly for rare attack categories and unseen network traffic.

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Umasree001/AI-Based-Cybersecurity-Intrusion-Detection.git
cd AI-Based-Cybersecurity-Intrusion-Detection
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

On Windows, activate it using:

```powershell
.\venv\Scripts\Activate.ps1
```

### 3. Install dependencies

Navigate to the `ML Pro` directory:

```bash
cd "ML Pro"
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

### 4. Run the dashboard

```bash
streamlit run app.py
```

Open the local URL displayed in your terminal.

**Note:** The project may require model files and datasets to be available in the expected locations before all features work correctly.

## 📁 Project Structure

```text
AI-Based-Cybersecurity-Intrusion-Detection/
├── ML Pro/
│   ├── app.py
│   ├── feature_extractor.py
│   ├── flow_builder.py
│   ├── live_capture.py
│   ├── live_monitor.py
│   ├── predict.py
│   ├── train_multiclass.py
│   ├── verify_model.py
│   ├── models/
│   ├── notebooks/
│   ├── results/
│   └── requirements.txt
├── .devcontainer/
└── README.md
```

## 🔮 Future Enhancements

- Improve detection of rare attack classes.
- Evaluate generalization on independent network traffic.
- Enhance alerting and monitoring features.
- Improve dashboard visualizations and usability.
- Add deployment and model-version management.

## ⚠️ Disclaimer

This project is intended for educational and research purposes. Predictions are not a guarantee that traffic is safe or malicious. Use network monitoring only on systems and networks you are authorized to access.

## 👩‍💻 Author

**Project:** AI-Based Cybersecurity Intrusion Detection & Threat Prediction System

Developed as an academic Machine Learning and Cybersecurity project.
