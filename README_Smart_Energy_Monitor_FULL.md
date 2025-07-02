
#  Smart Energy Monitor – IoT-Based Embedded System Project

This project is a **cloud-connected, simulated Smart Energy Monitoring System** designed using the **Particle Photon microcontroller**, Particle Cloud, and a custom-built web dashboard. It enables real-time appliance control, simulated energy tracking, overload detection, scheduling, and smart energy tips — all without requiring real electrical hardware.

>  Built for the CSC3328 Embedded Systems course.

---

##  Project Structure

```
Smart_Energy_Monitor/
├── firmware/        # Embedded C code for Photon Particle
├── dashboard/       # HTML, CSS, and JS files (frontend)
├── paper/           # Final IEEE-style report (DOC)
├── poster/          # Academic poster (PPT)
├── README.md

```

---

## Key Features

- Real-time control of simulated appliances: Heater, Fridge, AC
- Potentiometer-based temperature simulation triggers automatic heater/AC control
- Overload detection using blinking LED (if simulated load > 2000W)
- Live energy usage graphs (Chart.js)
- Daily consumption & cost estimation
- Appliance scheduling (on/off at specific times)
- Smart energy-saving tip generator
- CSV log export of usage history

---

##  Technologies Used

| Layer            | Tech Stack                             |
|------------------|-----------------------------------------|
| Microcontroller  | Particle Photon (Wi-Fi enabled)         |
| Firmware         | Embedded C/C++ using Particle Cloud SDK |
| Communication    | Particle Cloud API (HTTPS, JSON)        |
| Frontend         | HTML, CSS, JavaScript, Chart.js         |
| Simulation       | Potentiometer + LEDs (no real appliances) |

---

## Dashboard Preview

> A responsive web UI that communicates with the cloud-connected microcontroller in real time.

![Energy Icon](https://uxwing.com/wp-content/themes/uxwing/download/nature-and-environment/energy-green-icon.png)

- Toggle appliances remotely
- View power usage graph
- Schedule actions
- Receive live warnings and tips

---

## 📄 Documentation

-  `Ouajjou_Zhiri_Toreis_Paper.doc` — Full technical report (IEEE format)
-  `poster embedded systems project.ppt` — Presentation poster
-  `Firmware_Final.txt` — Source code for microcontroller
-  `SmartEnergyMonitor_Final_Embedded.html` — Frontend dashboard

---

##  Testing & Results

-  Dashboard-to-device response time: ~1 second
-  Accurate temperature-based automation
-  Overload detection triggered when total simulated wattage exceeds 2000W
-  Scheduler executed actions with <1 second drift
-  CSV logs matched usage accurately

---

##  Comparison with Real-World Solutions

| Feature                   | Traditional Meters | Commercial Smart Meters | This Project |
|---------------------------|---------------------|--------------------------|--------------|
| Real-time Feedback        | ❌                  | ✅                       | ✅           |
| Hardware-Free Simulation  | ❌                  | ❌                       | ✅           |
| Scheduling + Logging      | ❌                  | ✅                       | ✅           |
| Cost                      | High                | High                     | Low / Free   |

---

## Future Improvements

- Integrate actual power sensors (voltage/current)
- Add user authentication to the dashboard
- Build mobile app version
- Use ML for predictive usage alerts
- Add email notifications for overloads

---

## 👩‍💻 Contributors

- **Fatima Zahra Zhiri** -
- **Oumaima Ouajjou** — 
- **Kenza Toreis** —

---

## How to Run the Project Locally

### 1. Photon Particle Microcontroller Setup
- Flash the firmware from `firmware/Firmware_Final.txt` to your Particle Photon using the Particle Web IDE or CLI.
- Ensure the device is connected to Wi-Fi and registered to your Particle account.

### 2. Particle Cloud Configuration
- Create variables and functions using `Particle.variable()` and `Particle.function()` as per the firmware.
- Get your device ID and access token.

### 3. Web Dashboard
- Open `dashboard/SmartEnergyMonitor_Final_Embedded.html` in your browser.
- Edit the file to insert your:
  - `deviceID`
  - `accessToken`
- The dashboard will begin polling and controlling your Photon immediately.

---

## Security Considerations

This is an educational prototype. However, future secure deployments should:
- Implement HTTPS and user authentication
- Avoid hardcoding access tokens in frontend files
- Use environment variables and server-side API proxies
- Enable role-based access and audit trails

---

## Recommended Tools

- [Particle Web IDE](https://build.particle.io/)
- [Particle CLI](https://docs.particle.io/tutorials/developer-tools/cli/)
- [Chart.js](https://www.chartjs.org/)
- [Visual Studio Code](https://code.visualstudio.com/)
- [GitHub Pages](https://pages.github.com/) – For hosting the dashboard

---


