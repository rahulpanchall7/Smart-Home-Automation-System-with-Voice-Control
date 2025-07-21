<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Smart Home Automation System</title>
  <style>
    body { font-family: Arial, sans-serif; line-height: 1.6; background: #f9f9f9; margin: 0; padding: 20px; }
    h1, h2, h3 { color: #333; }
    code { background: #eee; padding: 2px 4px; border-radius: 3px; }
    pre { background: #eee; padding: 10px; border-radius: 5px; overflow-x: auto; }
    ul { margin-top: 0; }
    table { border-collapse: collapse; width: 100%; margin-bottom: 20px; }
    th, td { border: 1px solid #ccc; padding: 8px; text-align: left; }
    th { background-color: #f2f2f2; }
  </style>
</head>
<body>
  <h1>Smart Home Automation System with Voice Control</h1>

  <p>This project enables real-time control of smart home appliances through voice commands processed via cloud services and executed by an ESP32-based system over MQTT.</p>

  <h2>🚀 Overview</h2>
  <ul>
    <li>Voice-controlled automation of lights, fans, and more</li>
    <li>ESP32 microcontroller as the central unit</li>
    <li>Cloud-based STT (Speech-to-Text) with MQTT integration</li>
    <li>Secure communication using TLS</li>
  </ul>

  <h2>🔧 Features</h2>
  <ul>
    <li>Low-latency MQTT protocol</li>
    <li>Wake-word detection and cloud STT</li>
    <li>Peripheral management (relays, sensors)</li>
    <li>Energy-efficient and low-cost design</li>
  </ul>

  <h2>📦 Hardware Requirements</h2>
  <table>
    <tr><th>Component</th><th>Description</th></tr>
    <tr><td>ESP32-WROOM-32</td><td>Main microcontroller</td></tr>
    <tr><td>I²S MEMS Microphone</td><td>For voice input</td></tr>
    <tr><td>ULN2803A Relay Driver</td><td>Relay interfacing</td></tr>
    <tr><td>5V Relay Module</td><td>Control high-voltage devices</td></tr>
    <tr><td>DHT22</td><td>Temperature & Humidity Sensor</td></tr>
    <tr><td>PIR Sensor</td><td>Motion Detection</td></tr>
    <tr><td>LDR</td><td>Ambient Light Detection</td></tr>
    <tr><td>5V Power Supply</td><td>2A recommended</td></tr>
  </table>

  <h2>🧰 Software Stack</h2>
  <ul>
    <li><strong>ESP-IDF</strong> (C development framework)</li>
    <li><strong>MQTT over TLS</strong> for secure messaging</li>
    <li><strong>Google Assistant SDK</strong> or open STT</li>
    <li><strong>FreeRTOS</strong> task scheduling</li>
  </ul>

  <h2>🏗️ System Architecture</h2>
  <ol>
    <li>ESP32 detects wake-word using keyword spotting</li>
    <li>Captures 3s audio and sends it to cloud STT via MQTT</li>
    <li>Command intent extracted and sent back to ESP32</li>
    <li>ESP32 executes the corresponding action (relay/sensor)</li>
  </ol>

  <h2>📈 Performance</h2>
  <ul>
    <li>Voice Recognition Accuracy: ~92.5%</li>
    <li>Response Latency: ~180 ms average</li>
    <li>Power Consumption: 80–260 mA active, <10 µA deep sleep</li>
  </ul>

  <h2>🔒 Security</h2>
  <ul>
    <li>MQTT with TLS and client-side certs</li>
    <li>Encrypted communication for all command channels</li>
  </ul>

  <h2>📂 Getting Started</h2>
  <ol>
    <li>Clone the repo and flash <code>main.c</code> to ESP32</li>
    <li>Connect to Wi-Fi and MQTT broker</li>
    <li>Configure your voice assistant (or custom STT)</li>
    <li>Test commands like "Turn on the fan"</li>
  </ol>

  <h2>🔄 Future Work</h2>
  <ul>
    <li>On-device STT with TinyML</li>
    <li>Support for additional appliances</li>
    <li>Offline fallback and ML-based smart behavior</li>
  </ul>

  <h2>📜 License</h2>
  <p>Open-source under the <code>MIT License</code>. Free for personal and commercial use.</p>
</body>
</html>
