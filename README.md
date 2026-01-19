# Driver Drowsiness Detection System 🚗😴

A real-time **Driver Drowsiness Detection System** built using **Python**, **OpenCV**, and **Dlib**. This project detects eye blinks through facial landmarks and determines whether the person is **Active**, **Drowsy**, or **Sleeping**. When prolonged drowsiness or sleep is detected, an **audio alert** is triggered to prevent accidents.

---

## 👤 Author

**Akshaya Stephen**

---

## 📌 Project Overview

Drowsy driving is one of the major causes of road accidents. This project aims to reduce such risks by continuously monitoring the driver's eye movements using a webcam.

The system:

* Captures real-time video from the webcam
* Detects the face using Dlib’s face detector
* Extracts eye landmarks using a 68-point facial landmark predictor
* Calculates eye aspect ratios to detect blinks
* Classifies the driver's state as:

  * **Active** 😊
  * **Drowsy** 😐
  * **Sleeping** 😴
* Triggers an **audio alarm** if the driver remains drowsy or asleep for a sustained duration

---

## ⚙️ Technologies Used

* **Python 3**
* **OpenCV (cv2)** – Image processing and video capture
* **Dlib** – Face detection and facial landmark prediction
* **NumPy** – Mathematical operations
* **imutils** – Facial landmark utilities
* **winsound** – Alarm sound (Windows only)

---

## 🧠 How It Works

1. The webcam captures real-time video frames.
2. Each frame is converted to grayscale.
3. Dlib detects faces in the frame.
4. Facial landmarks are extracted using the 68-point landmark model.
5. Eye landmarks are used to calculate distances between eyelids.
6. A ratio is computed to detect:

   * No blink (eyes open)
   * Partial blink (drowsy)
   * Full blink (sleeping)
7. Based on blink frequency and duration:

   * Status text is displayed on the screen
   * Alarm is triggered if thresholds are exceeded

---

## 🚨 Alert Logic

| Eye State | Condition                     | Action         |
| --------- | ----------------------------- | -------------- |
| Active    | Eyes open normally            | No alert       |
| Drowsy    | Partial eye closure           | Warning status |
| Sleeping  | Eyes closed for long duration | Alarm sound    |

---

## ▶️ How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2. Install Dependencies

```bash
pip install opencv-python dlib imutils numpy
```

> ⚠️ Note: Installing **dlib** may require CMake and Visual Studio Build Tools on Windows.

### 3. Download Landmark Model

Download the file below and place it in the project directory:

* `shape_predictor_68_face_landmarks.dat`

### 4. Run the Script

```bash
python drowsiness_detection.py
```

Press **ESC** to exit the application.

---

## 🖥️ Output Screens

* Face detection with landmarks
* Status displayed: `Active`, `Drowsy`, or `SLEEPING !!!`
* Alarm alert when danger is detected

---

## ⚠️ Limitations

* Works best in good lighting conditions
* Alarm sound uses `winsound` (Windows-only)
* Single-face detection (designed for driver monitoring)

---

## 🚀 Future Enhancements

* Support for multiple faces
* Cross-platform sound alerts
* Head pose and yawning detection
* Mobile or embedded system integration
* AI model-based eye state classification

---

## 📜 License

This project is for **educational and learning purposes**.

---

⭐ If you find this project helpful, feel free to star the repository on GitHub!
