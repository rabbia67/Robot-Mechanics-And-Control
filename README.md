# Robot-Mechanics-And-Control
# 🤖 Robot Mechanics and Control – NAO Robot Kinematics

This repository contains implementations, simulations, and documentation for **Forward Kinematics (FK)** and **Inverse Kinematics (IK)** of the NAO humanoid robot's **arms** and **legs**.

---

## 📂 Repository Structure
```
├── Forward Kinematics/
│   ├── Arm Videos/        # Simulation videos for NAO robot arm
│   ├── Final codes/       # Python scripts for FK of arm and leg
│   └── Leg Videos/        # Simulation videos for NAO robot leg
│
├── Inverse Kinematics/
│   ├── Arm videos/        # Simulation videos for NAO arm IK
│   ├── Final Codes/       # Python scripts for IK of arm and leg
│   └── leg videos/        # Simulation videos for NAO leg IK
│
└── README.md
```

---

## 📜 Project Overview

### **Forward Kinematics**
Forward Kinematics involves calculating the **end-effector position and orientation** given the **joint parameters**.  
This project computes FK for:
- **NAO Robot Arm** (4 DOF: Shoulder Pitch, Shoulder Roll, Elbow Yaw, Elbow Roll)
- **NAO Robot Leg** (6 DOF: Hip Yaw-Pitch, Hip Roll, Hip Pitch, Knee Pitch, Ankle Pitch, Ankle Roll)

**Techniques Used:**
- Standard **Denavit–Hartenberg (DH) parameters**
- Homogeneous transformation matrices
- Simulation in **Webots**
- Angle control via a **Python GUI**  

---

### **Inverse Kinematics**
Inverse Kinematics determines the **joint angles** needed to place the end-effector at a desired position and orientation.

**Implemented for:**
- Arm IK: Calculates angles for desired hand positions.
- Leg IK: Calculates angles for desired foot positions.

**Methods Used:**
- Geometric IK for 2D simplifications
- Trigonometric solutions for multi-DOF limbs
- Simulation and validation in **Webots**

---

## 🛠 How to Run

### **Forward Kinematics**
1. Open **Webots** and load `nao_demo.wbt`.
2. Add FK Python code to Webots controller.
3. Run simulation and start the controller (listens on port `9999` for arm / `9998` for leg).
4. Open the **GUI script** in PyCharm or your preferred IDE.
5. Enter joint angles and send to Webots.

### **Inverse Kinematics**
1. Open **Webots** and load the NAO robot world.
2. Add IK Python code to Webots controller.
3. Specify desired end-effector position in the GUI.
4. Webots simulation updates NAO’s joints accordingly.

---

## 📊 Example Outputs

- **Forward Kinematics – Arm**
  - Computes final transformation matrix from shoulder to wrist.
  - Displays `(x, y, z)` coordinates for each pose.

- **Forward Kinematics – Leg**
  - Computes transformation from hip to ankle.
  - Supports multiple poses with varying joint angles.

- **Inverse Kinematics**
  - Returns joint angles for a given `(x, y, z)` target.
  - Supports both arm and leg configurations.

---

## 🎥 Demo Videos
- **FK Arm Simulation** → `Forward Kinematics/Arm Videos`
- **FK Leg Simulation** → `Forward Kinematics/Leg Videos`
- **IK Arm Simulation** → `Inverse Kinematics/Arm videos`
- **IK Leg Simulation** → `Inverse Kinematics/leg videos`

---

## 📜 License
This project is intended for educational purposes.
