Help File: Eufy Alerts Management Scripts
Overview
This document provides details on two Home Assistant automations and 
corresponding scripts designed to manage motion alerts for Eufy cameras.
The scripts are used to present the Eufy cameras to Alexa. 

Create the automations in Home Assistant and then create the scripts.

Automations

1. Snooze Eufy Alerts Automation:
Go to Settings > Automations & Scripts > Automations 
Click the blue "+ Create Automation" button on the bottom right to create a new automation.
Click "Create New Automation" and select "Start with an empty automation".
Click the 3 dots in the top right and select 
"Edit in YAML" to enter the automation configuration directly.
Paste in the contents of the snooze_eufy_alerts.yaml file.
Save the automation and ensure it is enabled.

2. Resume Eufy Alerts Automation:
Go to Settings > Automations & Scripts > Automations 
Click the blue "+ Create Automation" button on the bottom right to create a new automation.
Click "Create New Automation" and select "Start with an empty automation".
Click the 3 dots in the top right and select 
"Edit in YAML" to enter the automation configuration directly.
Paste in the contents of the resume_eufy_alerts.yaml file.
Save the automation and ensure it is enabled.

Scripts
1. Snooze Eufy Alerts Script:
Go to Settings > Automations & Scripts > Scripts
Click the blue "+ Create Script" button on the bottom right to create a new Script.
Click the 3 dots in the top right and select 
"Edit in YAML" to enter the Script configuration directly.
Paste in the contents of the snooze_eufy_alerts_script.yaml file.
Save the Script.

2. Resume Eufy Alerts Script:
Go to Settings > Automations & Scripts > Scripts
Click the blue "+ Create Script" button on the bottom right to create a new Script.
Click the 3 dots in the top right and select 
"Edit in YAML" to enter the Script configuration directly.
Paste in the contents of the resume_eufy_alerts_script.yaml file.
Save the Script.

Snooze Eufy Alerts: Temporarily disables motion alerts on specified cameras 
for a set duration. Default is 60 minutes.
Resume Eufy Alerts: Resumes motion alerts immediately on the same cameras after snoozing.

Usage
Manual Trigger:
Go to Settings > Automations & Scripts > Scripts in Home Assistant.
Find the script named Snooze Eufy Alerts and click Run Actions.

Alexa Integration:
Expose the script as a scene to Alexa and create a routine to trigger 
the scene with a custom phrase 
(e.g., "Alexa, snooze Eufy alerts").

Automation:
Use this script as part of an automation to snooze alerts during specific 
times or events.

Additional Notes
These scripts rely on the eufy_security.snooze service. Ensure the Eufy 
Security integration is properly configured in Home Assistant.
You can customize the snooze duration or affected cameras by editing the 
entity_id and snooze_time parameters in the scripts.