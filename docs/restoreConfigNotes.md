This is what needs to be done to setup this config on a fresh install of Home Assistant

Entire System:
Backup New Config Folder
- make a backup of the "config" folder that was created during the Home Assistant Install

Clone repo
- Ensure a backup of "config" has been made
- Delete everything in the config folder (this is needed to clone the repo)
- Clone this repo into the config folder `git clone "repo deets" . `
- Copy the following folders/files from the backup into the config folder
-- .HA_VERSION
-- .cloud
-- .storage
-- home-assistant.log
-- home-assistant_v2.db
-- secrets.yml
-- tts


Update Secrets
- Copy secrets over from local backup of secrets file


Change IP Address
- set IP address to a static IP

Re-setup Integrations and Add-ons
- HA should walk through setup for most integrations but manual setup is needed for some (or ones that are missing a secret)
Add-ons to install:
- Mosquitto (create logins that current devices are using)
- SSH & Web Terminal
- File editor

Before starting/restarting HA, use the config checker to see if everything is ok

UI:

Upload images
- upload images to the www/images folder

Reinstall HACS
https://hacs.xyz/docs/installation/prerequisites


Reinstall custom Lovelace cards
- bar-card                
- lovelace-auto-entities  
- mini-graph-card         
- surveillance-card
- button-card             
- lovelace-card-mod       
- mini-media-player
- decluttering-card       
- lovelace-layout-card    
- simple-weather-card
- upcoming-media-card
- battery-state-card
