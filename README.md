# 🏥 HASTURE – Intelligent Hospital Management System



## 📌 Overview
**HASTURE** is an intelligent **Hospital Management System (HMS)** that integrates:
- **Deep Learning (GRU)** for medical inventory forecasting  
- **High Utility Occupancy Pattern Mining (HUOMIL)** for identifying high-impact medical supplies  
- **Role-based dashboards** for administrators, doctors, in-charges, and inventory managers  

This project demonstrates how **Data Science, AI, and Web Technologies** can optimize hospital workflows, reduce resource wastage, and support **data-driven decision-making** in healthcare.  

---

## 🚀 Key Features
- 🔹 **Automated Hospital Workflows** → patient registration, ward allocation, inventory management  
- 🔹 **GRU-based Time Series Forecasting** → predicts monthly demand for medical inventory with low error (MSE ~9.74)  
- 🔹 **HUOMIL Algorithm** → mines inventory items with high utility & frequent use across patient records  
- 🔹 **Role-Based Dashboards** → different interfaces for doctors, admins, in-charges, and inventory managers  
- 🔹 **Real-Time Analytics** → occupancy rates, patient consultation trends, and resource utilization  
- 🔹 **Secure Access Control** → Django authentication and session management  

---

## 🧠 Data Science & Machine Learning
### GRU Forecasting
- Built using **TensorFlow/Keras**
- Learns from historical hospital inventory usage
- Produces **12-month demand forecasts**
- Achieved **MSE ≈ 9.74**

### HUOMIL Algorithm
- Custom implementation of **High Utility Occupancy Mining with Indexed List**
- Identifies items that are both **economically significant** and **frequently prescribed**
- Outputs **confidence scores and utility visualizations**

---

## 🛠️ Tech Stack
- **Backend:** Django, Python (NumPy, Pandas, scikit-learn, TensorFlow, Keras)  
- **Database:** MySQL  
- **Frontend:** HTML, CSS, Bootstrap, Matplotlib (for visualizations)  
- **Deployment:** Local server (future scope: cloud deployment)  

---Hospital_Project/
│── data/ # Sample hospital data (patients, inventory, consultations)
│── huomil.py # HUOMIL algorithm implementation
│── sample.py # GRU forecasting function
│── dashboards/ # Role-based views for admin, doctor, inventory manager
│── models.py # Django models (Patients, Inventory, Rooms, etc.)
│── templates/ # HTML dashboards and reports
│── requirements.txt # Dependencies
│── README.md # Project Documentation


---

## 📊 Sample Results
- **GRU Forecast**: Stable demand prediction for Amoxicillin and other key drugs  
- **HUOMIL Results**: Paracetamol, Amoxicillin, and Insulin identified as **top priority medicines**  
- **Ward Availability Dashboard**: Real-time tracking of patient bed occupancy (e.g., maternity ward at 62.5% load)  
- **Doctor Trends**: Visual analysis of patient consultations over time  

---

## 🔮 Future Enhancements
- ✅ Transformer-based forecasting models  
- ✅ Real-time anomaly detection in inventory usage  
- ✅ Mobile-friendly dashboards  
- ✅ NLP-based chatbot for hospital queries  
- ✅ API integration with existing HMS software  

---

## 📌 About Me
👋 Hi, I’m **Shamir Havas**, an aspiring **Data Scientist (Fresher)** passionate about applying **Machine Learning & Data Analytics** to solve real-world problems.  
This project was completed as part of my **M.Sc. (Data Science & Big Data Analytics)** at **Yenepoya (Deemed to be University), Mangalore**.  

- 📧 Email: shamirhavas.data@gmail.com  
- 💼 LinkedIn: [your LinkedIn profile]  
- 🖥️ Portfolio: [if available]  

---

## ⚡ How to Run
```bash
# Clone the repository
git clone https://github.com/yourusername/HASTURE.git
cd HASTURE

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run migrations
python manage.py migrate

# Start the server
python manage.py runserver


## 📂 Project Structure
