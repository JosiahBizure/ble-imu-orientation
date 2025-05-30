# BLE IMU Orientation Streamer (Arduino UNO R4)

This project streams orientation data over BLE using sensor fusion (Madgwick) on data from an LSM6DSO32 IMU. The orientation (roll, pitch, yaw) is sent in JSON format to a connected BLE central device.

## 📦 Hardware
- Arduino UNO R4 WiFi
- Adafruit LSM6DSO32 IMU (I2C)
- BLE-compatible phone or computer

## 🔧 Wiring
| IMU Pin | UNO R4 WiFi Pin |
|--------:|------------------|
| VIN     | 3.3V             |
| GND     | GND              |
| SDA     | SDA1 (D18)       |
| SCL     | SCL1 (D19)       |

*(Update if we end up using different pins or Wire vs. Wire1)*

# How to Use
# 1. Upload to your UNO R4
# . . .

## 📡 BLE Format

JSON packet sent over Nordic UART service:

```json
{
  "roll": 12.34,
  "pitch": -5.67,
  "yaw": 89.01
}