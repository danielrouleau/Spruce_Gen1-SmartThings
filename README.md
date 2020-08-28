# Spruce_Gen1-SmartThings
Gen1 Devices and SmartApps for new Samsung SmartThings app

# These Device Handlers and Schedule will work with the new Samsung SmartThings APP
# This is a preliminary release!!

The migration to the newest Samsing app has caused the Gen1 Spruce Controller device tile to break.
The Spruce Scheduler is also no longer visible for new installs in the app.

### v2.7 Latest 8-28-2020
- Zone devices refresh and operate correctly
- Pump/Master option added in “settings” so the zone will turn on/off anytime another zone is switched on/off
- “Dimmer” control added to Zones and is used to set the time before the zone will automatically turn off. Thsi does not effect schedules, and will be re-named at a later date so it is no longer a “Dimmer”

Importing this code into the SmartThings IDE will bring back functionality as listed below:
- Each zone will be populated as a seperate device
- Individual zones can be turned on and off
- Schedules can be setup and will run automatically or can be started manually
- Individual zones can be used in automations

Known issues:
- ~~Toggling a zone on or off does not refresh correctly, and shows "spinning/thinking" icon, however the zone does activate and toggling into the zone tile or out of the zone tile will "refresh" the state~~
- Apple iOS zone tile does not show "on", however inside the zone device screen will show "on" and "off" correctly

# Import the Device Handlers and SmartApp into your account

Follow the instructions from the following link to import the Device Handlers and Smartapp into your SmartThings account. The instructions and video are from https://konnected.io, **Spruce is in no way affiliated with Konnected**
- https://help.konnected.io/support/solutions/articles/32000022409-smartthings-enable-github-integration#
- Video: https://help.konnected.io/support/solutions/articles/32000022474-video-konnected-smartthings-installation-and-setup

You will add the GitHub Repository:
- Owner: PlaidSystems
- Name: Spruce_Gen1-SmartThings
- Branch: Master

Once complete, **Update from Repo**

# Updating Device and SmartApp code

The steps outlined in the links above use Github to “pull” the code into your account. Your SmartThings account will keep track of changes in the code, but will need to be told to “update”. This is done by repeating the Update from Repo button in the Device Handler and SmartApps pages of the SmartThings IDE at graph.api.smartthings.com/

You may **Update from Repo** anytime to get the latest code.

# Setup

1. The device handler code **Spruce Controller SST, Spruce zone** must be copied/imported into your IDE account and published following the instructions above.
2. The smartapp code **Spruce Scheduler SST** must be copied/imported into your IDE account and published following the instructions above.
3. Remove the Spruce Controller from the app, from the Spruce Device, go to **Edit** -> **Delete Device**
4. Add a new device with **Add Device** -> **Scan nearby** and then start the search on the Spruce controller
5. The app will find **Spruce Controller**
6. In the new Spruce Controller device, go to the preferences, select all Zones that you would like to use
7. Each zone will populate a new device in the app
8. If you have an exisiting Spruce Schedule installed from the Classic app, you may continue to use it. See section below for **Schedule Setup**

# Schedule Setup

You may continue to use your schedule carried over from the Classic app.  Or you may install a new schedule.

To use your existing schedule:
1. Open the schedule from the **SmartApps** menu in the new app
2. Go to **Schedule settings**
3. Set **Spruce Irrigation Controller** to the new Spruce Controller device.  **Do not select a zone device, the schedule will not run**
4. Press Next and Done to save.

To ceate a new schedule:
1. Go to **SmartApps**->**+** menu in the new app
2. Scroll down until you find **Spruce Scheduler SST**
3. Proceed to setup the same as the Classic app version.
