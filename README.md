
# XBee Web Control Interface (Pico W)

A modern and responsive web interface for controlling LEDs or other outputs via Raspberry Pi Pico W using XBee communication. Designed for real-time control with visual status indicators, this interface is lightweight and deployable on GitHub Pages or any static web server.

## 🌐 Live Interface

The interface consists of:
- A **main table view** with sequence data and control buttons.
- A **detail page** triggered when pressing `ON PROGRESS`, simulating a remote control request.

## ⚙️ Features

- 🔘 Button-based interaction for control (`OK`, `ON PROGRESS`)
- 🟡 Color-coded rows (Yellow for in-progress, Green for completed)
- 📡 Communication via HTTP to Pico W’s REST endpoint (`/led/on?pin=X`, `/led/off?pin=X`)
- 🔁 Automatic LED off when user navigates back to the home screen
- 📱 Fully responsive and easy to deploy on GitHub Pages

## 🚀 Deployment

1. Push the HTML file to a GitHub repository.
2. Enable GitHub Pages from repository settings (`main` branch → `/` root).
3. Update the `PICO_IP` variable in the script section to match your Pico W IP address:
   ```javascript
   const PICO_IP = "http://192.168.1.48";
   ```

## 📁 Folder Structure

```
xbeecontrol/
├── index.html   # Main interface file
```

## 🛠️ Requirements

- Raspberry Pi Pico W running HTTP server (e.g., MicroPython or C++)
- XBee module connected to Pico W
- Static hosting (GitHub Pages, Netlify, etc.)

## 📷 Preview

![Interface Screenshot](preview.png)

## 📌 Example Use

Used in manufacturing, testing stations, or assembly lines where human-machine interaction is needed for confirmation or diagnostics.

## 📝 License

MIT License
