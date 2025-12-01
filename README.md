# 🌿 PioGreen - Pioneering Green Intelligence

**PioGreen** is a mobile application that uses Artificial Intelligence and Machine Learning to promote sustainable agriculture.  
It helps identify plants, detect plant diseases, and classify sustainable farming methods — aiming to make farming more efficient, data-driven, and eco-friendly.



## 📘 Project Overview

Agriculture is one of the most important industries for human survival, but it faces serious challenges like crop diseases, overuse of resources, and unsustainable practices.  
PioGreen aims to assist farmers, students, and researchers by providing a smart, AI-powered tool that supports better agricultural decision-making through image classification and sustainability insights.

The app has three core modules:
1. **Plant Detection** – Identify the type of plant using AI-based image classification.  
2. **Plant Disease Detection** – Detect plant leaf diseases and provide information on symptoms and prevention.  
3. **Sustainable Farming Classifier** – Suggest sustainable farming practices based on plant and crop data.



## 🎯 Objectives

- Build an easy-to-use mobile app that applies AI to support green agriculture.  
- Use computer vision models to identify plant species and diseases from images.  
- Encourage sustainable practices through intelligent recommendations.  
- Help farmers and students learn about sustainable farming with technology.



## 🚀 Features

| Module | Functionality | Dataset Used | Model Type |
|--------|----------------|---------------|-------------|
| 🌿 **Plant Detection** | Identifies plant species from image | LeafSnap / Flavia | MobileNetV3 / EfficientNet-Lite |
| 🍂 **Plant Disease Detection** | Detects crop diseases from leaves | PlantVillage (Kaggle) | CNN (ResNet50 / EfficientNet) |
| 🌾 **Sustainable Farming Classifier** | Classifies farm fields as sustainable or not | Sustainable Farm Dataset / EuroSAT | Binary CNN Classifier |



## 🧠 How It Works

1. **User uploads or captures an image** (leaf, plant, or field).  
2. The image is **preprocessed** (resized, normalized).  
3. The app’s 3 modules run in sequence using **TensorFlow Lite models**.  
4. **Results are displayed**:  
   - Plant name  
   - Disease (if any)  
   - Sustainability score  
   - Eco-friendly farming tips  




## 🎨 App UI Structure

| Screen | Description |
|--------|--------------|
| 🌱 **Splash Screen** | Animated logo “PioGreen – Pioneering Green Intelligence” |
| 📸 **Home / Upload Screen** | Upload or capture plant/farm image |
| 🧠 **Analysis Screen** | Displays progress while models infer results |
| 📊 **Result Dashboard** | Shows identified plant, disease, sustainability score, and eco-tips |
| 🌿 **Tips Section** | Curated and AI-generated sustainable farming recommendations |



## ⚙️ Tech Stack

| Layer | Technology |
|-------|-------------|
| **Frontend (Mobile)** | Flutter (Dart) |
| **ML Models** | TensorFlow / Keras → TensorFlow Lite |
| **Model Deployment** | TFLite Interpreter in Flutter |
| **Backend (Optional)** | Flask API / Firebase |
| **Database (Optional)** | Firebase Realtime / Firestore |
| **Image Processing** | OpenCV / Pillow |



## 🧩 Datasets

| Module | Dataset | Size | Classes | Source |
|--------|----------|-------|----------|--------|
| **Plant Detection** | LeafSnap / Flavia | ~30K | 30–50 species | [LeafSnap](https://leafsnap.com/dataset/) |
| **Disease Detection** | PlantVillage | ~54K | 38 | [Kaggle Dataset](https://www.kaggle.com/datasets/emmarex/plantdisease) |
| **Sustainability Detection** | Sustainable vs Non-Sustainable Farms | ~27K | 2 | [Kaggle Dataset](https://www.kaggle.com/datasets/d4rklucif3r/sustainable-vs-non-sustainable-farms) |



## 🔧 Model Training Summary

1. **Preprocessing**
   - Image resizing (224×224)
   - Normalization (0–1 scaling)
   - Data augmentation (rotation, zoom, flip)

2. **Training**
   - Optimizer: Adam
   - Loss: Categorical Crossentropy
   - Epochs: 25–50 (depending on dataset size)
   - Batch size: 32
   - Early stopping with validation monitoring

3. **Conversion**
   - Trained `.h5` or `.pt` → `.tflite`
   - Quantization (for smaller mobile model size)
   - Integrated using `tflite_flutter` plugin in Flutter



## 🌍 Sustainability Impact

**PioGreen** aligns with UN Sustainable Development Goals:
- **SDG 2:** Zero Hunger  
- **SDG 12:** Responsible Consumption & Production  
- **SDG 15:** Life on Land  

By empowering farmers and agri-students with plant health and eco-awareness insights, it promotes a **greener, smarter future**.



## 📊 Sample Output

**Input:** Photo of a tomato leaf in a crop field  
**Output:**
🌿 Plant: Tomato (Solanum lycopersicum)
🍂 Disease: Leaf Curl Virus (Confidence: 91%)
🌾 Sustainability: Sustainable (Eco Index: 0.82)
💡 Suggestion: Use neem extract spray and organic compost.



## 💡 Future Enhancements
- 📍 Geo-tagging farms using location data  
- ☁️ Cloud-based model inference for faster results  
- 🧬 Crop growth tracker for recurring scans  
- 🔔 Push notifications with eco-farming reminders  



## 🧑‍💻 Author
**👩‍💻 Vidhi N. Pateliya**  
Final Year, Computer Science Engineering (AI Specialization)    
 

 
## ✨ Tagline
> “**PioGreen** — Pioneering Green Intelligence for a Sustainable Tomorrow.” 🌍💚
