# 🎤 Arduino Nano 33 BLE Sense - Voice-Controlled LED with Edge Impulse

<p align="center">
  <img width="410" height="260" alt="image" src="https://github.com/user-attachments/assets/32add870-18a0-4b51-a934-33752d2ab136" />
</p>

This project uses **Edge Impulse** to train and deploy a machine learning model on the **Arduino Nano 33 BLE Sense**.  
By recognizing spoken color names (in Spanish), the board controls its onboard RGB LEDs and changes their color accordingly.  

---

## 🚀 Features  
- 🎙️ Voice recognition using a model trained on **Edge Impulse Web Platform**  
- 🌐 Supports Spanish color names:  
  - **Rojo** → 🔴 Red LED  
  - **Azul** → 🔵 Blue LED  
  - **Verde** → 🟢 Green LED  
  - **Amarillo** → 🟡 Yellow LED (Red + Green)  
- ⚡ Real-time inferencing with onboard microphone (PDM)  
- 💡 LED color updates based on the **highest prediction probability**  

---

## 🛠️ Hardware Requirements  
- Arduino Nano 33 BLE Sense  
- Micro-USB cable  

---

## 📦 Software Requirements  
- Arduino IDE  
- Edge Impulse Web Platform (for training and deploying the model)  
- Edge Impulse Inference SDK (from `.zip` deployment)  

---

## ⚡ Setup Instructions  
1. **Train your model** using the **Edge Impulse Web Platform**:  
   - Record audio samples for each color word (*rojo, azul, verde, amarillo*).  
   - Train and test your model in Edge Impulse Studio.  
   - Deploy it as an **Arduino library (`.zip`)** and install it in the Arduino IDE.  

2. **Upload code**:  
   - Clone this repository or copy the `.ino` code into your Arduino IDE.  
   - Install the required Arduino libraries:  
     - `Edge Impulse Inference SDK` (from the `.zip` in step 1)  

3. **Run the project**:  
   - Connect your Arduino Nano 33 BLE Sense via USB.  
   - Upload the sketch to your board.  
   - Open the **Serial Monitor** at `115200 baud` to view predictions.  

---

## 🎨 How It Works  
1. The microphone captures audio input.  
2. The trained **Edge Impulse model** processes the audio and classifies which color was spoken.  
3. The onboard RGB LED updates to the detected color:  

<div align="center">

| Spoken Word (Spanish) | LED Output                               |
|------------------------|------------------------------------------|
| **Rojo**               | 🔴 Red                                  |
| **Azul**               | 🔵 Blue                                 |
| **Verde**              | 🟢 Green                                |
| **Amarillo**           | 🟡 Yellow (Red + Green) *(when no sound)* |

</div>

---


## Demo







<p align="center">
  <img src="https://github.com/user-attachments/assets/bf858112-76dc-42fc-85ab-d541c4a9e6e3" alt="demo" />
</p>



