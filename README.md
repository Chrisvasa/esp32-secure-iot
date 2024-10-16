# **secure-sensor-hub**

A lightweight ESP32-based system for securely collecting and transmitting temperature and humidity data over HTTPS. Designed with FOTA (Firmware Over-The-Air) support, the platform ensures reliable and encrypted data transmission to cloud services or databases like InfluxDB, while also providing secure and efficient firmware updates.

## **Features**
- **Secure Data Transmission:** Uses HTTPS for encrypting and securely sending temperature and humidity data from ESP32 to a Raspberry Pi hosting InfluxDB and Grafana.
- **FOTA (Firmware Over-The-Air):** Supports secure remote firmware updates via HTTPS.
- **Real-Time Monitoring:** Connects with InfluxDB for data storage and Grafana for visualization.
- **Raspberry Pi Compatible:** Optimized to integrate with a Raspberry Pi running InfluxDB and Grafana.

## **Requirements**
- **Hardware:**
  - ESP32 microcontroller
  - DHT22 (or other temperature/humidity sensor)
  - Raspberry Pi with InfluxDB and Grafana installed
- **Software:**
  - ESP-IDF or Arduino IDE
  - InfluxDB and Grafana for data storage and visualization
  - Python or Node.js for proxy (if necessary)

## **Installation and Setup**

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/Chrisvasa/esp32-secure-iot.git
   ```
2. **ESP32 Firmware:**
   - Install the necessary libraries for HTTPS and FOTA support.
   - Upload the code to your ESP32 using ESP-IDF or Arduino IDE.

3. **Set Up InfluxDB and Grafana on Raspberry Pi:**
   - Install InfluxDB and Grafana on your Raspberry Pi.
   - Create a new InfluxDB database for storing sensor data.
   - Set up a Grafana dashboard to visualize the data.

4. **Network Configuration:**
   - Configure your ESP32 to connect to your WiFi network.
   - Ensure the Raspberry Pi’s IP address is accessible from the ESP32.

## **FOTA Updates**
To perform a FOTA update:
1. Prepare the new firmware file.
2. Use the HTTPS endpoint to send the firmware to the ESP32 device.
3. The ESP32 will verify the firmware and update itself securely.

## **Usage**
Once set up, the ESP32 will:
- Periodically collect temperature and humidity data.
- Send the data securely over HTTPS to your InfluxDB instance on the Raspberry Pi.
- Visualize the data in real-time using Grafana.

## **Future Improvements**
- Add support for additional sensors (e.g., air quality, light sensors).
- Improve data aggregation and visualization in Grafana.
- Implement MQTT for optional data transmission.

## **License**
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
