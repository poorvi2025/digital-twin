# 📡 DigitalTwin-6G: Digital Twin for Semantic Communication in 6G Networks Using Deep Learning

A research prototype implementing a **Digital Twin-based Semantic Communication system** for 6G networks using Deep Learning (ResNet-18), dynamic 2-Server 10-Node topology simulation, real-time Plotly telemetry mirroring, time-series LSTM channel forecasting, and proactive adaptive control.

---

## 🛠️ Project Structure

```text
DigitalTwin-6G/
│
├── data/
│   ├── cifar10/               # Local CIFAR-10 dataset
│   ├── dataset.py             # Dataset verification & DataLoader pipeline
│   └── README.md
│
├── models/
│   ├── resnet_semantic.py     # ResNet-18 semantic feature extractor
│   ├── deep_jscc.py           # Deep JSCC CNN autoencoder & noise channel
│   └── dt_lstm.py             # Time-series LSTM channel predictor
│
├── semantic/
│   ├── feature_extractor.py   # Feature extraction API pipeline
│   └── semantic_packet.py     # Semantic packet builder & encapsulation
│
├── network/
│   ├── topology.py            # 2 Content Servers + 10 Nodes topology
│   ├── server.py              # Server 1 & Server 2 objects
│   ├── node.py                # Node N1..N10 objects & telemetry metrics
│   ├── telemetry.py           # Synthetic 6G telemetry generator
│   └── routing.py             # Semantic router (Server X -> Node Y -> Receiver)
│
├── digital_twin/
│   ├── twin.py                # Digital Twin engine & Plotly interactive graph
│   ├── state.py               # Dynamic state mirror & historical telemetry
│   └── predictor.py           # Digital Twin LSTM predictor integration
│
├── communication/
│   ├── channel.py             # Physical AWGN & Rayleigh fading channel
│   └── transmission.py        # Transmission runner over noise channels
│
├── control/
│   └── adaptive_controller.py # Proactive closed-loop profile switcher
│
├── evaluation/
│   └── metrics.py             # SSIM, PSNR, BER, MAE/RMSE calculation
│
├── experiments/
│   ├── train_resnet.py        # ResNet-18 model evaluation script
│   ├── train_jscc.py          # Deep JSCC evaluation script
│   └── train_lstm.py          # LSTM predictor experiment script
│
├── dashboard/
│   ├── app.py                 # Main Streamlit dashboard entry point
│   └── pages/
│       ├── 1_Dataset.py       # Phase 1 dataset explorer
│       ├── 2_Semantic_Extraction.py # Phase 2 & 3 ResNet extractor
│       ├── 3_Network_Topology.py   # Phase 5 network topology
│       ├── 4_Digital_Twin.py       # Phase 6 & 7 Digital Twin & Plotly graph
│       ├── 5_Communication.py      # Phase 4 & 8 semantic packet transmission
│       ├── 6_Prediction.py         # Phase 9 & 10 LSTM predictor & control
│       └── 7_Evaluation.py         # Phase 11 & 12 quantitative metrics
│
├── results/
│   ├── models/                # Model checkpoint directory
│   ├── plots/                 # Exported plot figures
│   └── metrics/               # Benchmarking results
│
├── requirements.txt
├── README.md
└── main.py
```

---

## 🏃 Quick Start

```powershell
# 1. Run main CLI test script
python main.py

# 2. Launch Interactive Streamlit Control Room Dashboard
streamlit run dashboard/app.py
```
