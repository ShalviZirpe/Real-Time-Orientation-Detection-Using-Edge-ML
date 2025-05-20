# RealTime Orientation Detection Using EdgeML
motion detection using a machine learning model on STM32L476RG, EDGE ML

---

# Features

Motion data logger code: Reads motion sensor data (e.g., accelerometer, gyroscope) and logs it for training.
motion data deployer ocde: Runs an ML model on STM32 using CMSIS-DSP or X-CUBE-AI to classify motion events.


# Hardware Used

- Microcontroller: STM32L476RG
- Motion Sensor: (e.g., LSM6DS3, MPU6050, or onboard IMU)
- other:  serial interface for data logging/sd card

---

# Software Requirements

- [STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html)
- CMSIS-DSP or X-CUBE-AI (for ML deployment)
---

# Workflow

# 1. Data Collection 
- Collect raw sensor data (acceleration, gyroscope, etc.)
- Label the data based on activity 
- Store as `.csv` or transmit via UART to host machine

# 2. Model Training
- Preprocess data 
- Train model 
- Export as `.tflite`, `.onnx`, or convert using STM's X-CUBE-AI

# 3. Model Deployment
- Convert trained model to C using X-CUBE-AI or CMSIS-DSP
- Integrate into STM32 firmware
- Compile and flash to board

---


