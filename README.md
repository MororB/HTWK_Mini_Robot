# 🤖 Mini-Roboter für die Hochschullehre  

Dieser kleine mobile Roboter wurde als **offene Lehrplattform** für Hochschulen entwickelt.  
Er ermöglicht Studierenden praxisnahes Lernen in den Bereichen **Robotik, Echtzeitsysteme und Industrie 4.0**, ohne hohe Kosten oder sicherheitskritische Einschränkungen.  
<p align="center">
  <img src="https://github.com/user-attachments/assets/7ba99f74-1f75-402f-9623-048474f4d45d" alt="Mini Roboter" width="400">
</p>



---
## 📑 Inhaltsverzeichnis  
- [Zielsetzung](#-zielsetzung)  
- [Hardwareübersicht](#-hardwareübersicht)  
- [Software & Steuerung](#-software--steuerung)  
- [Einsatz in der Lehre](#-einsatz-in-der-lehre)  
- [Nützliche Ressourcen](#-nützliche-ressourcen)  
- [Weiterentwicklung](#-weiterentwicklung)  

---

## ✨ Zielsetzung  
- Vermittlung von Grundlagen zu **Sensorik, Aktorik und Steuerung**  
- Einfache Integration in **ROS 2**-basierte Lehrveranstaltungen  
- **Didaktisch sinnvoll** durch transparente Hardware und offene Software  
- **Kosteneffizient und sicher** durch Miniaturbauweise und reduzierte Geschwindigkeit  

---

## 🔧 Hardwareübersicht  
- **ESP32** – Hauptcontroller, WLAN-fähig, Micro-ROS Unterstützung  
- **ATtiny 212** – dezentrale Motorsteuerung, entlastet den ESP32  
- **28BYJ-48 Schrittmotoren** + ULN2003-Treiberplatinen  
- **Sensorik**  
  - APDS-9960: Farb-, Gesten- und Abstandssensor  
  - HC-SR04: Ultraschallsensor für Hinderniserkennung  
  - GY-9250 (IMU): Lage- und Bewegungserfassung  
  - IR-Kommunikationsmodul: Datenübertragung zwischen Robotern  
  - Mikroschalter (Bumper) für Kollisionserkennung  
- **Weitere Komponenten**  
  - OLED-Display (128×64 Pixel)  
  - LED-Statusanzeigen  
  - Passiver Piezo-Buzzer für akustische Signale  
- **Energieversorgung**  
  - 18650-Li-Ion-Akku mit Lade- und Schutzmodul  
  - Konstant 5V-Ausgang für alle Module  
- **Chassis**  
  - Modularer 3D-Druck, minimalistisch, anpassbar  
  - Einfache Wartung, Teile leicht austauschbar  
---
## 📂 3D Druck-Teile
- **1x** [Hauptplatte]()
- **4x** [Lagerung Ober]()
- **4x** [Lagerung Unten]()
- **2x** [Welle]()
- **2x** [Motor Clip]()
- **1x** [Lademodul und Stecker Gehäuse]()
- **1x** [Murmel]()
- **1x** [Murmel Halter]()
- **2x** [Reifen]()
- **2x** [Rad]()
- **2x** [Bumper Deckel]()
- **1x** [Bumper Gehäuse Links]()
- **1x** [Bumper Gehäuse Rechts]()
- **1x** [Bumper]()

---

## 🖥️ Software & Steuerung  
- **Micro-ROS** auf ESP32 zur direkten Einbindung in **ROS 2**  
- **Dezentrale Motorsteuerung** über ATtiny-Controller per UART  
- Volle Unterstützung für **ROS 2 Topics, Nodes und Sensorintegration**  
- Didaktische Beispiele:  
  - Hindernisvermeidung mit Ultraschall  
  - Linien-/Farberkennung mit APDS-9960  
  - IMU-basierte Lagebestimmung  
  - Kommunikation zwischen mehreren Robotern  

---

## 📚 Einsatz in der Lehre  
Der Mini-Roboter wird in Praktika und Projekten eingesetzt, um:  
- **Grundlagen der ROS 2-Architektur** zu vermitteln (Publisher/Subscriber, Topics, Nodes)  
- **Echtzeitsysteme** und deren Anforderungen an Steuerung & Kommunikation erlebbar zu machen  
- **Eigene Projektideen** umzusetzen, z. B. autonome Navigation oder Sortieraufgaben  
- Einen **Vergleich zu professionellen Robotern** (z. B. TurtleBot 4) herzustellen  

---
## 📖 Nützliche Ressourcen  

### 🔹 ROS 2  
- [ROS 2 Dokumentation – Tutorials Übersicht](https://docs.ros.org/en/humble/Tutorials.html)  
- [Einführung in ROS 2 Nodes](https://docs.ros.org/en/humble/Tutorials/Beginner-CLI-Tools/Understanding-ROS2-Nodes.html)  
- [Einführung in ROS 2 Topics](https://docs.ros.org/en/humble/Tutorials/Beginner-CLI-Tools/Understanding-ROS2-Topics.html)  
- [ROS 2 Installation (Ubuntu 22.04, Humble)](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debs.html)  

### 🔹 Micro-ROS  
- [micro-ROS – Übersicht & Dokumentation](https://micro.ros.org)  
- [micro-ROS PlatformIO Repository](https://github.com/micro-ROS/micro_ros_platformio)  
- [micro-ROS Setup Repository](https://github.com/micro-ROS/micro_ros_setup)  

### 🔹 Praktische Robotikplattformen  
- [TurtleBot 4 – Clearpath Robotics](https://clearpathrobotics.com/turtlebot-4/)  
- [TurtleBot 4 User Manual](https://turtlebot.github.io/turtlebot4-user-manual/)  
- [TurtleBot 4 Simulator](https://turtlebot.github.io/turtlebot4-user-manual/software/turtlebot4_simulator.html#turtlebot-4-simulator)  

### 🔹 Zusätzliche Ressourcen  
- [Ubuntu 22.04 Download](https://releases.ubuntu.com/22.04/)  
- [VirtualBox – Offizielle Downloads](https://www.virtualbox.org/wiki/Downloads)  
- [28BYJ-48 Schrittmotor Tutorial](https://elektro.turanis.de/html/prj143/index.html)  

---
## 🔮 Weiterentwicklung  
- Erweiterbare Sensorik (z. B. LiDAR, Time-of-Flight)  
- Flexiblere Chassis-Architektur mit Lochraster- oder Schienensystem  
- Optimierte Pinbelegung des ESP32 für robusteren Betrieb  
- Multi-Roboter-Szenarien mit ROS 2-Kommunikation  

---

