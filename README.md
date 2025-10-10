**Sign Language Detection Web Application**

A comprehensive **real-time sign language detection system** combining computer vision, deep learning, and web technologies.  
This project leverages **MediaPipe Holistic**, **LSTM sequence modeling**, and a **Flask web interface** to recognize sign language gestures from live webcam input, visualize predictions, and manage user data.

---

** Project Overview
**
The system is designed to explore applications in **human-computer interaction (HCI)**, **assistive technology**, and **gesture-based communication**. It provides:

- Real-time hand, face, and body landmark detection.
- Gesture recognition using temporal sequences of keypoints.
- Interactive web interface for users and administrators.
- User authentication, dashboard, and data management through **MySQL**.

---

 **Features
**
- **Web Interface**: Flask-based interface with login, signup, admin panel, dashboards, and pie chart visualizations.  
- **Real-time Detection**: Uses **MediaPipe Holistic** to extract pose, hand, and face keypoints from webcam feed.  
- **Deep Learning Gesture Recognition**: LSTM-based sequence model trained to detect multiple sign language gestures (`bye`, `hello`, `help`, `iamsleepy`, `iloveyou`, `shocked`, `thanks`).  
- **Motion Detection**: Highlights meaningful frame changes to improve prediction accuracy.  
- **Visual Feedback**: Displays gesture probabilities as overlay bars on webcam frames.  
- **Database Integration**: MySQL-powered user management (signup, login, update, delete, admin monitoring).  
- **Session Management**: Secure session handling to distinguish users and admins.

---

** Project Structure**

├── MyApp.py # Main Flask application
├── models/ # Trained models (e.g., LSTM weights)
│ └── May10_Second.h5
├── templates/ # HTML templates (index.html, login.html, admin.html, etc.)
├── style/ # CSS / static assets
├── FinalDataSet/ # Folder containing gesture images for training/sequence generation
└── README.md

yaml
Copy code

---

** Installation**

1️. **Clone the repository:**
```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
2️. Install dependencies:
bash
Copy code
pip install flask opencv-python mediapipe numpy matplotlib mysql-connector-python tensorflow
3️. Set up MySQL database:
Create a database named actions_language.
Create a users table with fields: id, name, email, age, password.
4️. Place trained model files (e.g., May10_Second.h5) in models/.
5️. Run the app:
bash
Copy code
python MyApp.py
6️. Open http://127.0.0.1:5000 in your browser.

 **How It Works**
-> Users can signup/login to access the dashboard.
-> Admin can view all users, update/delete records, and view pie charts of user demographics.
-> Users can access the webcam detection page:
-> MediaPipe extracts pose, hand, and face landmarks.
-> Landmark sequences are passed to the LSTM model for gesture recognition.
-> Real-time feedback is displayed on the screen with probability overlays.
-> Motion detection ensures predictions are only highlighted when significant movement occurs.

**Research & Application**
This project demonstrates applied research in gesture recognition, enabling:
Communication aids for hearing-impaired individuals.
Prototype HCI systems for real-time gesture-based control.
Data collection for behavioral analysis and AI model training.
It showcases integration of computer vision, deep learning, and web technologies in an end-to-end applied AI system.

**Technologies Used**
Python 3
Flask – Web framework
MediaPipe Holistic – Pose, hand, and face detection
OpenCV – Video capture and visualization
TensorFlow / Keras – LSTM sequence modeling
MySQL – User management and data storage
Matplotlib – Data visualization (pie charts)

**Future Scope**
Extend to real-time multi-user recognition.
Integrate with AR/VR interfaces for immersive gesture control.
Expand the dataset for comprehensive sign language coverage.
Deploy on cloud for remote accessibility and scalability.

** Author**
Avantika Nepal


yaml
Copy code
