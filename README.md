🎤 Arduino Nano 33 BLE Sense - Voice-Controlled LED with Edge Impulse

<img width="410" height="260" alt="image" src="https://github.com/user-attachments/assets/32add870-18a0-4b51-a934-33752d2ab136" />


This project uses Edge Impulse to train and deploy a machine learning model on the Arduino Nano 33 BLE Sense.
By recognizing spoken color names (in Spanish), the board controls its onboard RGB LEDs and changes their color accordingly.

🚀 Features

Voice recognition using Edge Impulse trained model.

Recognizes Spanish color names such as:

Rojo → Red LED

Azul → Blue LED

Verde → Green LED

Amarillo → Yellow LED (combination of red + green)

Real-time inferencing with onboard microphone (PDM).

LED color updates based on the highest prediction probability.

🛠️ Hardware Requirements

Arduino Nano 33 BLE Sense

Micro-USB cable

📦 Software Requirements

Arduino IDE

Edge Impulse Web Platform (for training and deploying the model)

⚡ Setup Instructions

Train your model using the Edge Impulse Web Platform:

Record audio samples for each color word (rojo, azul, verde, amarillo).

Train and test your model in Edge Impulse Studio.

Deploy it as an Arduino library (.zip) and install it in the Arduino IDE.

Clone this repository or copy the .ino code into your Arduino IDE.

Install the required Arduino libraries:

Edge Impulse Inference SDK (via the .zip from step 1)

Connect your Arduino Nano 33 BLE Sense via USB.

Upload the sketch to your board.

Open the Serial Monitor at 115200 baud to view predictions.

🎨 How It Works

The microphone captures audio input.

The trained Edge Impulse model processes the audio and classifies which color was spoken.

The onboard RGB LED updates to the detected color:

Spoken Word (Spanish)	LED Output
Rojo	🔴 Red
Azul	🔵 Blue
Verde	🟢 Green
Amarillo	🟡 Yellow (Red + Green) [Just when there is no sound]
