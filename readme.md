# Naruto Plant Monitoring System

## Overview

This README outlines a simplified architecture inspired by Naruto characters to create an efficient and lightweight solution for monitoring the well-being of plants. The system comprises various components, each named after a Naruto character, reflecting their roles in ensuring the health of the plants.

## Components

### 1. Shikamaru - ESP8266 Module with LM393

- The "Shikamaru" module is attached to each plant, monitoring soil moisture levels.
- When moisture reaches a critical level, "Shikamaru" initiates a POST request to signal the need for attention.

### 2. Jiraiya - Clojure Webhook

- "Jiraiya" serves as a robust Clojure-based Webhook server, managing incoming POST requests from the ESP8266 modules.
- It processes humidity data and triggers notifications as required.

### 3. Tsunade - Python Notification Application

- Named after strength and swiftness, "Tsunade" listens to "Jiraiya" and sends notifications to Telegram.
- The application periodically checks the plant status stored in the local database.

### 4. Sakura - Local Database

- "Sakura" functions as a local database, symbolizing care and record-keeping, storing plant states and watering events.
- "Tsunade" queries this database to determine the necessity for notifications.

### 5. Kakashi - Security and Resilience

- Basic security measures, inspired by "Kakashi's" wisdom, are implemented to validate received data.
- For resilience, an exponential retry mechanism ensures the reliable delivery of notifications.

## Stories and Definition of Done (DoD)

### 1. Configuration of ESP8266 with LM393

- **DoD:** Each "Shikamaru" is connected to the LM393 module and efficiently monitors soil moisture.

### 2. Development of Clojure Webhook (Jiraiya)

- **DoD:** "Jiraiya" can receive POST requests, process data, and trigger notifications as needed.

### 3. Simple Implementation of Python Notification Application (Tsunade)

- **DoD:** "Tsunade" can listen to "Jiraiya" and send notifications to Telegram based on local database data.

### 4. Local Database (Sakura)

- **DoD:** A local database "Sakura" is set up to store the state of plants and watering events.

### 5. Basic Tests

- **DoD:** Basic tests are conducted to ensure communication between components is working correctly.

### 6. Simple Documentation

- **DoD:** Minimal documentation includes setup and basic operation instructions for the system.

This Naruto-inspired plant monitoring system offers a seamless blend of technology and the ninja spirit, ensuring the well-being of your plants with efficiency and style.

