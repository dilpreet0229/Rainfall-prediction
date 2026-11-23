RainFall Prediction — Machine Learning & AI Weather Studio (Indian Locations)
An interactive, beginner-friendly Rainfall Prediction Web Application built with Python (FastAPI, Scikit-learn) for data preprocessing and machine learning, and React.js (Vite, Recharts) for a modern, responsive user interface.

Trained on 24,070 official weather records, comparing 5 Scikit-Learn algorithms, featuring Random Forest Classifier (90.69% Test Accuracy), Indian location datasets with automatic parameter filling, multi-language support, clickable analytics bar charts, and a floating interactive AI help assistant.

🌟 Key Features
Exact Reference UI Matching:

Header: Royal blue banner styled with "RainFall Prediction — MACHINE LEARNING & GENERATIVE AI (INDIAN DATASET)".
Left Panel (Rainfall Prediction Form): 20 meteorological parameters (Date, Location, Min/Max Temp, Rainfall, Evaporation, Sunshine, Wind Gust Speed/Direction, Wind Speed 9am/3pm, Humidity 9am/3pm, Pressure 9am/3pm, Cloud Cover, Temp, and Rain Today/Tomorrow).
Automatic Parameter Auto-Fill: Selecting any Indian city immediately pre-fills all 20 fields with typical meteorological readings.
Indian Scenario Chips: 1-click test buttons for:
🌧️ Mumbai Monsoon (Heavy Downpour)
☀️ Delhi Sunny (Dry & Warm)
🌦️ Kolkata Pre-Monsoon Showers
⛈️ Kochi Heavy Monsoon Rain
☀️ Jaipur Clear Desert Weather
🎲 Random City
Predict Button: Teal button with real-time computation and active loading state.
Clean Standby & Dynamic Visual Reveal:

Before Prediction: Shows a clean, inviting "Ready for Prediction" card. Visual outcome images are hidden initially.
After Prediction: Dynamically reveals the vibrant prediction card:
Sunny Outcome: Magenta card with "TOMORROW WILL BE A SUNNY DAY!" and an animated smiling cartoon sun with radiant beams (or screenshot photo).
Rainy Outcome: Dark rainstorm card with "TOMORROW WILL BE A RAINY DAY!" and an animated smiling rain cloud with falling droplets.
Confidence Gauge: Progress bar showing sunny confidence % or rain probability %.
Clickable Visual Analytics Bar Charts (Recharts & Matplotlib Style):

Algorithm Benchmark Bar Chart:
Compares 5 algorithms: Random Forest (90.69%), Gradient Boosting (89.30%), Extra Trees (88.85%), Decision Tree (88.60%), Logistic Regression (85.25%).
Click any bar to open an in-depth view showing Accuracy, F1-Score, Precision, Recall, and the full Confusion Matrix evaluated on 4,814 test records!
Atmospheric Feature Importance Bar Chart:
Relative Humidity (32%), Pressure (24%), Cloud Cover (18%), Wind Speed (14%), Temperature (12%).
Click any feature bar to open meteorological physics explanations and decision threshold guides.
Forecast Probability Distribution Bar:
Click the card to open a detailed breakdown of how many trees in the 100-tree ensemble voted Dry vs Rain.
Multi-Language Support (7 Languages):

Switch between:
🇬🇧 English
🇮🇳 हिन्दी (Hindi)
🇮🇳 বাংলা (Bengali)
🇮🇳 मराठी (Marathi)
🇮🇳 తెలుగు (Telugu)
🇮🇳 தமிழ் (Tamil)
🇮🇳 ગુજરાતી (Gujarati)
Instantly translates verdict headings, labels, metrics, and chart titles.
Floating App Guide & Help AI Chatbot:

A discreet floating button in the bottom-right corner (💬 App Guide & Help AI).
Opens an assistant with 1-click FAQ answers:
💡 How to use this app?
🌧️ How to test a Rainy forecast?
☀️ How to test a Sunny forecast?
🤖 Which ML model is used?
📊 What do the charts show?
🇮🇳 Which Indian cities are supported?
Plus free-text question answering!
🚀 Quick Start Guide
Step 1: Start the Backend (FastAPI)
cd backend
& "C:\Users\swaya\AppData\Local\Programs\Python\Python313\python.exe" -m uvicorn main:app --reload --port 8000
Backend runs at http://127.0.0.1:8000 (API docs at http://127.0.0.1:8000/docs).

Step 2: Start the Frontend (React + Vite)
In a new terminal:

cd frontend
npm run dev
Open your browser and navigate to http://localhost:5173/.

📁 Project Structure
Rainfall Prediction/
│
├── backend/
│   ├── main.py               # FastAPI application & REST endpoints
│   ├── genai_engine.py       # Meteorological reasoning engine
│   ├── preprocessing.py      # Data cleaning, imputation, scaling, IQR analysis
│   ├── train_model.py        # 5 Scikit-learn algorithms & evaluation
│   ├── predict.py            # Model inference engine
│   ├── visualizations.py     # Data provider for Recharts
│   ├── test_pipeline.py      # Automated backend verification test
│   └── saved_models/         # Serialized best model (.joblib)
│
├── frontend/
│   ├── index.html            # Web app entry point
│   ├── vite.config.js        # Vite dev server configuration
│   └── src/
│       ├── App.jsx           # Main reference UI with 2 panels & chart integration
│       ├── components/
│       │   ├── WeatherIllustration.jsx  # Smiling Sun & Rain Cloud illustrations
│       │   ├── AnalyticsCharts.jsx      # Clickable Matplotlib-style Bar Charts
│       │   └── HelpChatbot.jsx          # Floating App Guide AI assistant
│       ├── services/
│       │   ├── api.js                   # FastAPI backend integration
│       │   └── indianWeatherDataset.js  # Indian cities dataset & translations
│       └── styles/
│           └── index.css                # Styling & responsive design system
│
├── data/
│   └── weather_data.csv      # 24,070 weather observations
│
└── Weather data.xlsx         # Original Excel dataset
💡 How to Demonstrate
Open http://localhost:5173/.
Notice the initial clean "Ready for Prediction" standby card on the right.
Select an Indian city from the dropdown (e.g., Delhi, NCR) or click "Delhi Sunny" — all 20 weather parameters populate automatically.
Click "Predict Rainfall" — the right card reveals "TOMORROW WILL BE A SUNNY DAY!" with the cute smiling cartoon sun and 91.7% sunny confidence.
Scroll down to the Machine Learning Analytics & Visual Charts:
Click on the "Random Forest" bar — an in-depth modal opens showing the accuracy (90.69%), F1 score (90.77%), and the complete confusion matrix on 4,814 test records!
Click on the "Humidity 3pm" bar — read the plain-English meteorological explanation of why humidity is the #1 rain driver.
Click on the Forecast Probability Bar — view the 100-tree ensemble vote breakdown.
Now select "Mumbai Monsoon" or "Kochi Heavy Rain" and click "Predict Rainfall" — the card reveals "TOMORROW WILL BE A RAINY DAY!" with animated falling raindrops and 88%+ rain probability!
Switch the language dropdown at the top (e.g. to हिन्दी or বাংলা) to show full multi-language output.
Click "App Guide & Help AI" in the bottom-right corner to demonstrate the interactive helper chatbot!
