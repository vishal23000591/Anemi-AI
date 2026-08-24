# AnemiAI – Smart Anaemia Screening and Non-Invasive Haemoglobin Prediction

AnemiAI is a machine learning–based healthcare application designed to enable non-invasive screening of anaemia and estimation of haemoglobin (Hb) levels using images captured from a standard camera. The system analyzes color features extracted from the lower eyelid region and predicts both anaemia status and approximate haemoglobin concentration without requiring blood samples.

---

## Project Overview

Anaemia is a widespread health condition affecting millions globally, especially in low-resource and rural areas where access to laboratory diagnostics is limited. Traditional haemoglobin tests require invasive blood collection and laboratory infrastructure. AnemiAI aims to address this challenge by providing a cost-effective, accessible, and non-invasive screening tool using computer vision and machine learning techniques.

The project utilizes RGB pixel intensity analysis and a dual-output neural network to classify anaemia and predict haemoglobin levels from eyelid images.

---

## Key Features

* Non-invasive anaemia screening using camera-based images
* Haemoglobin level prediction using machine learning regression
* Anaemia classification (Anaemic / Non-Anaemic)
* Real-time image capture through a web interface
* Backend API for prediction and processing
* Scalable design suitable for rural and telemedicine applications

---

## System Architecture

The system follows a modular architecture consisting of:

1. **Image Capture** using a web camera
2. **Preprocessing** and RGB feature extraction
3. **Feature Normalization** using trained scalers
4. **Dual-Output Neural Network**:
   * Classification for anaemia detection
   * Regression for haemoglobin prediction
5. **REST API** for frontend-backend communication

---

## Technologies Used

### Backend

* Python
* Flask
* TensorFlow / Keras
* NumPy
* Scikit-learn
* MongoDB (for user authentication and data storage)

### Frontend

* React.js
* HTML, CSS, JavaScript
* Webcam API for image capture

### Machine Learning

* Feedforward Neural Network
* RGB feature-based prediction
* StandardScaler and MinMaxScaler

---

## Dataset Description

The dataset consists of records containing:

* Percentage of Red pixel values
* Percentage of Green pixel values
* Percentage of Blue pixel values
* Haemoglobin (Hb) level
* Anaemia status (Yes / No)

The dataset was preprocessed, normalized, and split into training and testing sets before model training.

---

## Model Training

* **Input features:** Red, Green, Blue pixel percentages
* **Outputs:**
   * Binary classification for anaemia
   * Continuous regression for haemoglobin level
* **Loss functions:**
   * Binary Crossentropy for classification
   * Mean Squared Error for regression
* **Optimizer:** Adam

---

## Installation and Setup

1. **Clone the repository:**

   ```bash
   git clone https://github.com/vishal23000591/Anemi-AI.git
   ```

2. **Navigate to the project directory:**

   ```bash
   cd Anemi-AI
   ```

3. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the backend server:**

   ```bash
   python app.py
   ```

5. **Start the frontend application:**

   ```bash
   cd frontend
   npm install
   npm start
   ```

---

## API Endpoint

### Prediction Endpoint

```bash
POST /predict
```

**Request Body:**

```json
{
  "red": 45.2,
  "green": 29.1,
  "blue": 25.7
}
```

**Response:**

```json
{
  "anaemia": "Yes",
  "hb": 9.8
}
```

---

## Results

* High accuracy in anaemia classification
* Reliable haemoglobin estimation within acceptable clinical range
* Consistent performance across varied RGB input samples

---

## Applications

* Preliminary anaemia screening
* Rural and remote healthcare
* Telemedicine platforms
* Health camps and awareness programs
* Research and academic use

---

## Limitations

* Dependent on image quality and lighting conditions
* Not a replacement for laboratory blood tests
* Requires further clinical validation

---

## Future Enhancements

* Deep learning–based eyelid segmentation
* Mobile application integration
* Clinical-grade dataset expansion
* Integration with electronic health records
* Explainable AI for medical transparency

---

## Authors

**Vishal S**
Register Number: 212223110063
Department: BE Computer Science and Engineering (IoT)
Saveetha Engineering College

## License

This project is developed for academic and research purposes.

---

## Status

**Current Version:** Alpha
**Last Updated:** 2024

This project is currently in active development. We welcome contributions and improvements from the community!