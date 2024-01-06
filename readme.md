# Green-House Monitoring System

Welcome to Green-House, a comprehensive plant monitoring system designed to bring the spirit of nature into your home! Inspired by the efficiency of ninja services, Green-House ensures your plants receive optimal care.

## Overview

Green-House is a monorepo comprising several services for decentralized plant monitoring. Each service has a specific role, contributing to a seamless and robust gardening experience.

### Services

1. **ESP8266 Module (Shikamaru):**
   - Responsible for local soil moisture monitoring for each plant.
   - Sends data to the central server for processing.

2. **Clojure Webhook (Jiraiya):**
   - Processes data from ESP8266 modules.
   - Triggers notifications based on soil moisture levels.
   - Central component for managing plant data.

3. **Python Notification App (Tsunade):**
   - Listens to notifications triggered by Jiraiya.
   - Sends notifications to Telegram.
   - Periodically checks the plant status in the local database.

4. **Local Database (Sakura):**
   - Stores and manages plant states and watering events.
   - Accessed by Tsunade for notification decisions.

5. **Security and Resilience Service (Kakashi):**
   - Implements basic security checks for incoming data.
   - Provides a simple retry mechanism for notification delivery.

## Getting Started

Follow these steps to set up Green-House on your system:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/Green-House.git
   cd Green-House

