# Tâm Trí Số (Digital Mind) 🧠🛡️

> **An Edge-Computing AI solution to combat doomscrolling and protect smart device users' mental health.**

**Project Lead / Designer:** Phan Bao Tin  
**Date:** August 2026 | Ho Chi Minh City  

---

## 📖 1. Executive Summary

In the era of the "Attention Economy," social media algorithms are designed to maximize user retention, leading to severe mental health consequences such as smartphone addiction, doomscrolling, and cognitive decline. 

**Tâm Trí Số** is developed to serve as an invisible AI shield, acting as a personal "psychological guardian." The software passively collects on-screen behavioral data, analyzing it to detect negative, cyclical scrolling patterns. Once detected, the AI applies micro-psychological "nudges" to help users naturally break free from these states—without feeling manipulated or compromising their privacy.

## 🏗️ 2. System Architecture & Technology

To overcome barriers related to sensitive data privacy, the project implements a decentralized processing model optimized for edge devices.

### 2.1. Edge AI (Artificial Intelligence at the Edge)
Behavioral data collection (such as scroll speed, typing force, and dwell time) is **never** sent to the cloud, preventing any risk of data leakage. The Machine Learning model is optimized using tools and SDKs from the **NVIDIA Developer Program**, ensuring the AI runs smoothly directly on the device's NPU/GPU with minimal energy consumption.

### 2.2. Flexible Backend Architecture
While the AI processes data locally on the client, the system requires a backend for user account management, settings synchronization, and anonymous log collection (if explicitly permitted by the user) to improve the ML models. **Supabase** is utilized as the cloud infrastructure, providing robust PostgreSQL capabilities, secure Authentication, and real-time Edge Functions.

## 🧠 3. Psychological Intervention (UI/UX & Behavioral Design)

The greatest challenge of this project is not the code, but behavioral psychology. If users feel forced, they will experience "Reactance" and uninstall the app. The project adheres to 4 core principles:

| Principle | Practical Implementation Strategy |
| :--- | :--- |
| **1. Pre-commitment** | Establish a "Pact" upon installation. Users choose intervention scenarios: *"If I mindlessly scroll TikTok for over 40 minutes, turn the screen black and white."* When the AI intervenes, it is simply executing the user's own commands. |
| **2. Nudge Theory** | Instead of abruptly locking apps, the AI gradually increases "friction": Reducing brightness by 15%, switching the screen to Grayscale to lower dopamine spikes, or requiring a slow 3-second slider swipe to continue viewing content. |
| **3. Explainable AI** | Always explain the reason for intervention with subtle notifications: *"Your scroll speed increased by 50%, you seem stressed. Let's close your eyes for 10 seconds."* This turns the AI into a friendly medical assistant. |
| **4. Override Switch** | Always provide a "Pause AI for 2 hours" button. Ultimate control belongs to the human, giving them complete peace of mind while using the app. |

## ⚙️ 4. Technical Integration Approaches (OS & App)

Due to OS sandboxing limitations on iOS/Android, injecting into other apps is highly complex. The project explores the following approaches:

*   **Approach 1 - Accessibility Service (Android):** Utilize Accessibility permissions to read on-screen content and overlay color filters/warnings on top of target apps like Facebook and TikTok.
*   **Approach 2 - Custom Browser / Launcher:** Build a dedicated web browser or Launcher through which users access social media, granting the AI full control over the DOM and displayed content.
*   **Approach 3 - Metadata Analysis:** A content-agnostic approach. Instead of knowing *what* the user is watching, the AI analyzes accelerometer data (device shaking/holding posture) and swipe speed to evaluate stress levels.

## 📚 5. References & Research Materials

The foundational theories and technical directions of this project are inspired by:

### 5.1. Implemented Projects & Products
*   **Mindstrong Health (Passive Digital Phenotyping):** A pioneer in using smartphones to measure mental health by tracking typing metrics (pressure, speed, backspaces) without reading message content.
*   **Center for Humane Technology:** Led by Tristan Harris, providing "Humane Design" principles. Their documentary *"The Social Dilemma"* serves as core inspiration.
*   **Apple Screen Time & Android Digital Wellbeing:** OS-level solutions. Open-source analysis of Android's App Usage Stats serves as baseline input data for the AI.

### 5.2. Scientific Papers & Research
*   *“Digital Phenotyping: Evolving Mental Health from Clinic to Smartphone”* by Thomas R. Insel (2017).
*   *“Doomscrolling during COVID-19: The negative association between daily social and traditional media consumption and mental health”* (Global Challenges, 2020).
*   *“Nudging for Digital Wellbeing: A systematic literature review”* - Evaluates UI/UX interventions to combat device addiction.
