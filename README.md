Face Recognition with Real-Time Database
This project is a Real-Time Face Recognition Attendance System built using Python, OpenCV, and Firebase Realtime Database. It detects faces through a webcam, matches them with pre-registered face encodings, and stores attendance records in real time.

🛠️ Tech Stack
Frontend: OpenCV (Python-based GUI with live webcam)

Backend: Python

Database: Firebase Realtime Database

Libraries:

cv2 (OpenCV)

face_recognition

firebase_admin

datetime, os, pickle

🚀 Features
✅ Real-time face detection using webcam
✅ Face recognition using pre-trained encodings
✅ Attendance marking with timestamp
✅ Live sync with Firebase Realtime Database
✅ Option to add new student face encodings
✅ Duplicate entry prevention per day

📁 Project Structure
bash
Copy
Edit
FaceRecognitionRealTimeDatabase/
│
├── face_recognition_module.py     # Handles encoding & face recognition logic
├── firebase_utils.py              # Contains Firebase DB setup and operations
├── main.py                        # Entry point for running the attendance system
├── add_face.py                    # Utility to register new students
├── encodings/                     # Stores face encodings as pickle files
├── images/                        # Stores images of registered students
├── requirements.txt               # Python libraries needed
└── README.md                      # This file
🔧 Setup Instructions
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/your-username/FaceRecognitionRealTimeDatabase.git
cd FaceRecognitionRealTimeDatabase
2. Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
3. Firebase Setup
Go to Firebase Console

Create a new project

Go to Project Settings > Service Accounts → Generate new private key

Save serviceAccountKey.json in the root of this project

Enable Realtime Database in test mode

4. Add Student Face Images
Put images in the /images folder with filenames as student names

Run the following command to generate encodings:

bash
Copy
Edit
python add_face.py
5. Run the Attendance System
bash
Copy
Edit
python main.py
📊 Firebase Structure (Example)
json
Copy
Edit
{
  "Attendance": {
    "StudentName": {
      "2025-05-11": "09:34:22"
    }
  }
}
