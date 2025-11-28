# 🚀 **SpeedTest – Android Internet Speed Monitor**

A lightweight and reusable Internet Speed Test module for Android.
Built with **Kotlin**, **Coroutines**, and **Jetpack Compose**, it continuously measures **real-time download speed** and exposes it through a simple API + optional UI widget.

---

## ⭐ Features

* 🔄 Real-time internet speed monitoring
* ⚡ Automatic background speed measurement
* 🧩 Reusable in any Android project
* 📊 Jetpack Compose speed widget included
* 🎯 Lightweight, no dependencies
* 📦 Simple API

---

## 📁 Project Structure

```
speedtest/
│
├── SpeedTestMonitor.kt     # Continuous speed monitor
├── SpeedTestUtil.kt        # One-time speed test utility
│
└── ui/
    └── SpeedWidget.kt      # Optional Compose UI widget
```

---

## 📌 Installation

Copy the `speedtest` folder into:

```
app/src/main/java/com/yourproject/
```

Add permission in `AndroidManifest.xml`:

```xml
<uses-permission android:name="android.permission.INTERNET"/>
```

---

## 🛠 Usage

### **1. Start Monitoring**

```kotlin
val monitor = SpeedTestMonitor()
monitor.start()
```

### **2. Observe Speed in Compose**

```kotlin
val speed by monitor.speedFlow.collectAsState()
Text("%.2f Mbps".format(speed))
```

### **3. Use Built-In Speed Widget**

```kotlin
SpeedWidget(monitor)
```

### **4. Stop Monitoring**

```kotlin
monitor.stop()
```

---

## 📦 One-Time Speed Test

```kotlin
val speed = SpeedTestUtil.measureSpeedOnce()
println("Speed: $speed Mbps")
```

---

## 🧱 Built With

* Kotlin
* Coroutines
* Jetpack Compose
* StateFlow

---

## 🤝 Contributing

Pull requests are welcome!
For major changes, please open an issue first to discuss what you would like to change.

---

## 📄 License

MIT License

---
