# 🌱 GreenTracker – AI-Based Plant Disease Detection System

GreenTracker is an **AI-powered web-based plant disease detection system** that helps users identify diseases in plants by analyzing images of their leaves.

The system uses **Machine Learning/Deep Learning-based image classification** to detect possible plant diseases and provides the user with the predicted disease information.

---

## 📌 Project Overview

Plant diseases can significantly affect crop production and plant health. Identifying diseases manually can be difficult, time-consuming, and requires expert knowledge.

**GreenTracker** provides a simple solution where a user can:

1. Upload an image of a plant leaf.
2. The AI model analyzes the image.
3. The system predicts the possible disease.
4. The result is displayed on the website.

The main goal of this project is to make plant disease detection **faster, easier, and accessible through a web interface**.

---

## 🎯 Objectives

- 🌱 Detect plant diseases from leaf images.
- 🤖 Use AI/ML for automated disease classification.
- 🖥️ Provide an easy-to-use web interface.
- ⚡ Reduce the time required for manual disease identification.
- 📊 Provide reliable prediction results.
- 🌾 Help farmers and plant owners identify potential diseases at an early stage.
- 🔬 Demonstrate the practical application of Artificial Intelligence in agriculture.

---

## ✨ Features

- 📷 Upload plant/leaf images.
- 🤖 AI-based disease prediction.
- 🌿 Plant disease classification.
- 📊 Prediction result display.
- 🖥️ User-friendly web interface.
- 📱 Responsive design.
- ⚡ Fast prediction.
- 🔄 Easy integration between frontend, backend, and AI model.
- 🌱 Potential for adding treatment/recommendation information.

---

## 🏗️ System Architecture

The basic workflow of GreenTracker is:

```text
                 ┌──────────────────┐
                 │      User        │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │  Web Interface   │
                 │   (Frontend)     │
                 └────────┬─────────┘
                          │
                     Upload Image
                          │
                          ▼
                 ┌──────────────────┐
                 │     Backend      │
                 │  Image Handling  │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │   AI/ML Model    │
                 │ Image Classifier │
                 └────────┬─────────┘
                          │
                     Prediction
                          │
                          ▼
                 ┌──────────────────┐
                 │ Prediction Result│
                 │ Disease + Score  │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │       User       │
                 └──────────────────┘
```

---

## 🛠️ Technologies Used

### Frontend

- HTML5
- CSS3
- JavaScript
- React.js *(if used in the final implementation)*

### Backend

- Node.js
- Express.js

### AI / Machine Learning

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- OpenCV
- Scikit-learn

### Database

- MongoDB *(if database functionality is implemented)*

### Development Tools

- Git
- GitHub
- VS Code
- Jupyter Notebook / JupyterLab
- Google Colab *(optional)*

---

## 🧠 AI Model

The core component of GreenTracker is the **plant disease classification model**.

The model is trained using images of healthy and diseased plant leaves.

### Model Workflow

```text
Dataset
   ↓
Image Collection
   ↓
Data Preprocessing
   ↓
Image Resizing
   ↓
Data Augmentation
   ↓
Train / Validation Split
   ↓
Model Training
   ↓
Model Evaluation
   ↓
Model Saving
   ↓
Web Integration
   ↓
Disease Prediction
```

---

## 📂 Dataset

The model requires a dataset containing images of plant leaves belonging to different disease classes.

Each image is associated with a particular class, such as:

```text
Plant Dataset
│
├── Healthy
│
├── Disease Class 1
│
├── Disease Class 2
│
├── Disease Class 3
│
└── Disease Class N
```

The dataset can be divided into:

- Training dataset
- Validation dataset
- Testing dataset

### Example Dataset Structure

```text
dataset/
│
├── train/
│   ├── Healthy/
│   ├── Disease_1/
│   ├── Disease_2/
│   └── Disease_3/
│
├── validation/
│   ├── Healthy/
│   ├── Disease_1/
│   ├── Disease_2/
│   └── Disease_3/
│
└── test/
    ├── Healthy/
    ├── Disease_1/
    ├── Disease_2/
    └── Disease_3/
```

---

## 🔄 Image Processing

Before an image is passed to the AI model, it may go through several preprocessing steps:

1. Image loading
2. Image resizing
3. Pixel normalization
4. Noise reduction *(if required)*
5. Data augmentation during training

For example:

```text
Original Image
      ↓
Resize Image
      ↓
Normalize Pixels
      ↓
Convert to Model Input
      ↓
AI Model
```

---

## 🧪 Model Training

The model is trained using labeled plant leaf images.

During training, the model learns visual patterns such as:

- Leaf color
- Spots
- Lesions
- Discoloration
- Texture
- Shapes
- Disease-specific patterns

The trained model is then evaluated using unseen test images.

---

## 📊 Model Evaluation

The model can be evaluated using different performance metrics:

### Accuracy

Measures the percentage of correctly classified images.

```text
Accuracy = Correct Predictions / Total Predictions
```

### Precision

Measures how many predicted positive cases are actually positive.

### Recall

Measures how many actual positive cases were correctly identified.

### F1-Score

Provides a balance between precision and recall.

### Confusion Matrix

A confusion matrix can be used to understand which disease classes are being correctly or incorrectly classified.

---

## 📁 Project Structure

A possible project structure is:

```text
GreenTracker/
│
├── frontend/
│   ├── public/
│   ├── src/
│   ├── index.html
│   └── package.json
│
├── backend/
│   ├── routes/
│   ├── controllers/
│   ├── models/
│   ├── uploads/
│   ├── server.js
│   └── package.json
│
├── model/
│   ├── plant_disease_model.h5
│   ├── class_names.json
│   └── model.py
│
├── dataset/
│   └── README.md
│
├── notebooks/
│   └── model_training.ipynb
│
├── screenshots/
│   ├── home.png
│   ├── upload.png
│   └── result.png
│
├── requirements.txt
├── README.md
└── .gitignore
```

> The exact structure may change depending on the final implementation.

---

# 🚀 Installation and Setup

## 1. Clone the Repository

```bash
git clone https://github.com/your-username/GreenTracker.git
```

Move into the project directory:

```bash
cd GreenTracker
```

---

## 2. Setup Python Environment

Create a virtual environment:

```bash
python -m venv venv
```

Activate the environment on Windows:

```bash
venv\Scripts\activate
```

For macOS/Linux:

```bash
source venv/bin/activate
```

---

## 3. Install Python Dependencies

```bash
pip install -r requirements.txt
```

---

## 4. Install Backend Dependencies

Move to the backend folder:

```bash
cd backend
```

Install dependencies:

```bash
npm install
```

---

## 5. Start the Backend

```bash
npm start
```

The backend server will start on the configured port.

Example:

```text
http://localhost:5000
```

---

## 6. Start the Frontend

Open another terminal:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

The frontend will be available at the URL shown in the terminal.

---

# 🖥️ How to Use

### Step 1

Open the GreenTracker website.

### Step 2

Click on:

```text
Upload Image
```

### Step 3

Select an image of a plant leaf.

### Step 4

Click:

```text
Detect Disease
```

### Step 5

The image is sent to the backend/model.

### Step 6

The AI model analyzes the image.

### Step 7

The predicted disease is displayed.

Example:

```text
Plant: Tomato

Prediction:
Tomato Leaf Disease

Confidence:
94.6%
```

---

# 🔌 API Workflow

The frontend communicates with the backend through an API.

Example workflow:

```text
Frontend
   │
   │ POST Image
   ▼
Backend API
   │
   │ Preprocess Image
   ▼
AI Model
   │
   │ Prediction
   ▼
Backend
   │
   │ JSON Response
   ▼
Frontend
```

Example response:

```json
{
  "plant": "Tomato",
  "disease": "Tomato Leaf Disease",
  "confidence": 94.6
}
```

---

# 🔐 Security Considerations

The application should consider the following security practices:

- Validate uploaded file types.
- Restrict maximum image size.
- Sanitize user input.
- Avoid storing unnecessary personal information.
- Secure API endpoints.
- Use environment variables for sensitive configuration.
- Do not upload sensitive credentials to GitHub.

---

# 🌐 Future Enhancements

GreenTracker can be further improved with:

- 🌱 Support for more plant species.
- 🦠 Detection of more diseases.
- 💊 Disease treatment recommendations.
- 🌦️ Weather-based disease risk prediction.
- 📍 Location-based agricultural recommendations.
- 📊 User history and prediction tracking.
- 👨‍🌾 Farmer-friendly multilingual interface.
- 📱 Mobile application.
- ☁️ Cloud deployment.
- 🔔 Disease alerts and notifications.
- 🧠 Improved deep learning models.
- 📈 Confidence and prediction analytics.

---

# ⚠️ Limitations

The prediction accuracy depends on:

- Quality of the uploaded image.
- Lighting conditions.
- Dataset quality.
- Number of disease classes.
- Training data diversity.
- Similarity between real-world images and training images.

The system should therefore be considered an **AI-assisted detection tool**, not a replacement for professional agricultural diagnosis.

---

# 👨‍💻 Team Members

| Name | Role |
|---|---|
| Kumar Harsh | Developer / AI & DS |
| Kishlay Kumar Dubey | Developer |
| Mehakpreet Kaur | Developer |
| Nandini | Developer |

---

# 🎓 Academic Project

**Project Name:** GreenTracker  
**Project Title:** AI-Based Plant Disease Detection System  
**Domain:** Artificial Intelligence & Data Science  
**Type:** Web-Based AI Application  

---

# 📜 License

This project is developed for educational and academic purposes.

You may modify and improve the project according to your requirements.

---

# ⭐ Contributing

Contributions and suggestions are welcome.

To contribute:

```bash
git fork
```

Create a new branch:

```bash
git checkout -b feature/new-feature
```

Make your changes and commit them:

```bash
git add .
git commit -m "Add new feature"
```

Push the branch:

```bash
git push origin feature/new-feature
```

Then create a Pull Request.

---

# 📬 Contact

For questions, suggestions, or collaboration, please open an issue in this repository.

---

## 🌱 GreenTracker

**Turning Artificial Intelligence into a smarter solution for plant health.**

⭐ If you find this project useful, consider giving the repository a star!
