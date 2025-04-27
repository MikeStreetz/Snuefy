# Help File: Eufy Alerts Management Scripts
## Note
To have a higher snooze duration than 1000 seconds you need to edit your services.yaml file on line 300 to change the max value to 43200.
SSH to Home Assistant and edit /config/custom_components/eufy_security/services.yaml

## Overview
This document provides details on two Home Assistant automations and corresponding scripts designed to manage motion alerts for Eufy cameras. The scripts are used to present the Eufy cameras to Alexa.

Create the automations in Home Assistant and then create the scripts.

---

## Automations

### 1. Snooze Eufy Alerts Automation
1. Go to **Settings > Automations & Scripts > Automations**.
2. Click the blue **"+ Create Automation"** button on the bottom right to create a new automation.
3. Click **"Create New Automation"** and select **"Start with an empty automation"**.
4. Click the 3 dots in the top right and select **"Edit in YAML"** to enter the automation configuration directly.
5. Paste in the contents of the `snooze_eufy_alerts.yaml` file.
6. Save the automation and ensure it is enabled.

### 2. Resume Eufy Alerts Automation
1. Go to **Settings > Automations & Scripts > Automations**.
2. Click the blue **"+ Create Automation"** button on the bottom right to create a new automation.
3. Click **"Create New Automation"** and select **"Start with an empty automation"**.
4. Click the 3 dots in the top right and select **"Edit in YAML"** to enter the automation configuration directly.
5. Paste in the contents of the `resume_eufy_alerts.yaml` file.
6. Save the automation and ensure it is enabled.

---

## Scripts

### 1. Snooze Eufy Alerts Script
1. Go to **Settings > Automations & Scripts > Scripts**.
2. Click the blue **"+ Create Script"** button on the bottom right to create a new script.
3. Click the 3 dots in the top right and select **"Edit in YAML"** to enter the script configuration directly.
4. Paste in the contents of the `snooze_eufy_alerts_script.yaml` file.
5. Save the script.

### 2. Resume Eufy Alerts Script
1. Go to **Settings > Automations & Scripts > Scripts**.
2. Click the blue **"+ Create Script"** button on the bottom right to create a new script.
3. Click the 3 dots in the top right and select **"Edit in YAML"** to enter the script configuration directly.
4. Paste in the contents of the `resume_eufy_alerts_script.yaml` file.
5. Save the script.

---

## Features

- **Snooze Eufy Alerts**: Temporarily disables motion alerts on specified cameras for a set duration (default is 12 hours or 43200 seconds).
- **Resume Eufy Alerts**: Resumes motion alerts immediately on the same cameras after snoozing.

---

## Usage

### Manual Trigger
1. Go to **Settings > Automations & Scripts > Scripts** in Home Assistant.
2. Find the script named **Snooze Eufy Alerts** and click **Run Actions**.

### Alexa Integration
- Expose the script as a scene to Alexa and create a routine to trigger the scene with a custom phrase (e.g., "Alexa, snooze Eufy alerts").

### Automation
- Use this script as part of an automation to snooze alerts during specific times or events.

---

## Additional Notes
- These scripts rely on the `eufy_security.snooze` service. Ensure the **Eufy Security integration** is properly configured in Home Assistant.
- You can customize the snooze duration or affected cameras by editing the `entity_id` and `snooze_time` parameters in the automations.
