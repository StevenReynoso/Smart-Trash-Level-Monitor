# 🗑️ Smart Trash Level Monitor

🚀 **An Arduino-based ultrasonic sensor system that monitors trash bin levels and displays the fill percentage on an LCD.**

## 📌 Project Overview
This project uses 3  **HC-SR04 ultrasonic sensor** to measure the height of trash inside a bin. The **Arduino** processes the sensor data, calculates the fill percentage, and displays it on a **LiquidCrystal I2C LCD screen**. Additionally, it logs the readings to the **Serial Monitor** for real-time debugging.

## 🎯 Features
✅ **Real-time trash level detection** using an ultrasonic sensor  
✅ **LCD display output** showing trash bin fill percentage  
✅ **Serial Monitor logging** for debugging and calibration  
✅ **Simple and efficient calculation method** for accurate level readings  
✅ **Modular and expandable** (can integrate WiFi/Bluetooth for remote monitoring)  

## 🔧 Hardware Components
- 🖥 **Arduino Uno** (or any compatible board)
- 📟 **16x2 I2C LCD Display**
- 📡 **3 HC-SR04 Ultrasonic Sensor**
- 🔌 **Jumper Wires**
- 🔋 **Power Supply**

## 📜 How It Works
1. The **HC-SR04 ultrasonic sensors** measure the distance from the sensors to the top of the trash, and each sensors travel time in microseconds is then used for the average calculation of room thats left in trash bin.
2. The distance is converted into **inches and centimeters**.
3. The fill percentage is calculated using:
   ```cpp
   trash = ((132.0 - inches) / (132.0 - 2.0)) * 100.0;

<html><body>
<!--StartFragment--><ul data-start="1548" data-end="1631"><li data-start="1548" data-end="1588"><code data-start="1550" data-end="1562">132 inches</code> → Bin is <strong data-start="1572" data-end="1581">empty</strong> (0%)</li>
<li data-start="1592" data-end="1631"><code data-start="1594" data-end="1604">2 inches</code> → Bin is <strong data-start="1614" data-end="1622">full</strong> (100%)</li>
</ul>
<ol start="4" data-start="1632" data-end="1797">
<li data-start="1632" data-end="1728">The fill percentage is displayed on the <strong data-start="1675" data-end="1689">LCD screen</strong> and printed to the <strong data-start="1709" data-end="1727">Serial Monitor</strong>.</li>
<li data-start="1729" data-end="1797">The system updates every <strong data-start="1757" data-end="1770">2 seconds</strong> for continuous monitoring.</li>
</ol>
<h2 data-start="1799" data-end="1826">🛠️ Installation &amp; Setup</h2>
<h3 data-start="1827" data-end="1858"><strong data-start="1831" data-end="1858">1️⃣ Wiring Instructions</strong></h3>
<div class="overflow-x-auto contain-inline-size">
Component | Arduino Pin
-- | --
(1) HC-SR04 Trigger | 6
(1) HC-SR04 Echo | 7
(2) HC-SR04 Trigger | 8
(2) HC-SR04 Echo | 9
(3) HC-SR04 Trigger | 10
(3) HC-SR04 Echo | 11
LCD SDA | A4
LCD SCL | A5

</div>
<h3 data-start="2010" data-end="2040"><strong data-start="2014" data-end="2040">2️⃣ Uploading the Code</strong></h3>
<ol data-start="2041" data-end="2462">
<li data-start="2041" data-end="2087">Install <strong data-start="2052" data-end="2067">Arduino IDE</strong> (if not installed).</li>
<li data-start="2088" data-end="2281">Install the required library for <strong data-start="2124" data-end="2135">I2C LCD</strong>:
<ul data-start="2140" data-end="2281">
<li data-start="2140" data-end="2227">Open <strong data-start="2147" data-end="2162">Arduino IDE</strong> → Go to <strong data-start="2171" data-end="2181">Sketch</strong> → <strong data-start="2184" data-end="2203">Include Library</strong> → <strong data-start="2206" data-end="2226">Manage Libraries</strong>.</li>
<li data-start="2231" data-end="2281">Search for <strong data-start="2244" data-end="2265">LiquidCrystal_I2C</strong> and install it.</li>
</ul>
</li>
<li data-start="2282" data-end="2317">Connect the <strong data-start="2297" data-end="2316">Arduino via USB</strong>.</li>
<li data-start="2318" data-end="2395">Upload the code in <a data-start="2340" data-end="2394" rel="noopener"><code data-start="2341" data-end="2366">smart_trash_monitor.ino</code></a>.</li>
<li data-start="2396" data-end="2462">Open the <strong data-start="2408" data-end="2426">Serial Monitor</strong> (<code data-start="2428" data-end="2439">9600 baud</code>) to see live readings.</li>
</ol>
<h2 data-start="2464" data-end="2482">📸 Project Demo</h2>
<p data-start="2483" data-end="2547">🚀 Coming soon! (Include an image or GIF of the working project)</p>
<h2 data-start="2549" data-end="2574">🚀 Future Improvements</h2>
<ul data-start="2575" data-end="2805">
<li data-start="2575" data-end="2654">📡 <strong data-start="2580" data-end="2599">IoT Integration</strong> → Send data to a cloud platform for remote monitoring.</li>
<li data-start="2655" data-end="2720">🔔 <strong data-start="2660" data-end="2683">Buzzer Alert System</strong> → Notify users when the bin is full.</li>
<li data-start="2721" data-end="2805">📊 <strong data-start="2726" data-end="2750">OLED Display Support</strong> → Improve visualization with graphical representation.</li>
</ul>
<hr data-start="2807" data-end="2810">
<h2 data-start="2812" data-end="2824">🏆 Author</h2>
<p data-start="2825" data-end="2957">👨‍💻 <strong data-start="2831" data-end="2849">Steven Reynoso</strong><br data-start="2849" data-end="2852">
🔗 GitHub: <a data-start="2863" data-end="2923" rel="noopener" target="_new" href="https://github.com/StevenReynoso">github.com/StevenReynoso</a><br data-start="2923" data-end="2926">
📩 Contact: [Your Email Here]</p>
<p data-start="2959" data-end="3082">💡 <em data-start="2962" data-end="3010">Feel free to fork this project and contribute!</em><br data-start="3010" data-end="3013">
📌 <strong data-start="3016" data-end="3078">If you like this project, don't forget to ⭐ star the repo!</strong> ⭐</p><!--EndFragment-->
</body>
</html>132 inches → Bin is empty (0%)
    2 inches → Bin is full (100%)

    The fill percentage is displayed on the LCD screen and printed to the Serial Monitor.
    The system updates every 2 seconds for continuous monitoring.

🛠️ Installation & Setup
1️⃣ Wiring Instructions
Component	Arduino Pin
(1) HC-SR04 Trigger | 6
(1) HC-SR04 Echo | 7
(2) HC-SR04 Trigger | 8
(2) HC-SR04 Echo | 9
(3) HC-SR04 Trigger | 10
(3) HC-SR04 Echo | 11
LCD SDA | A4
LCD SCL | A5
2️⃣ Uploading the Code

    Install Arduino IDE (if not installed).
    Install the required library for I2C LCD:
        Open Arduino IDE → Go to Sketch → Include Library → Manage Libraries.
        Search for LiquidCrystal_I2C and install it.
    Connect the Arduino via USB.
    Upload the code in smart_trash_monitor.ino.
    Open the Serial Monitor (9600 baud) to see live readings.

📸 Project Demo

🚀 

![image](https://github.com/user-attachments/assets/858a351e-c14b-46f9-acb2-a371c10d11b7)



🚀 Future Improvements

    📡 IoT Integration → Send data to a cloud platform for remote monitoring.
    🔔 Buzzer or small light Alert System → Notify users when the bin is full.

🏆 Author

👨‍💻 Steven Reynoso
🔗 GitHub: [github.com/StevenReynoso](https://github.com/StevenReynoso)
📩 Contact: sreynosowork.gmail.com
