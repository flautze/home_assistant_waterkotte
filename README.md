# Waterkotte Display using the pictures entity card
This Repository was created to share the setup of the pictures entity card to emulate/imitate the Waterkotte heatpump display overview in Home Assistant.
All but 2 sensors in use are originating from the below linked Waterkotte Integration.
My heatpump setup is pretty simple:
A1 Geo EcoTouch, no additional buffer or functions - apart from SG ready. SG ready was realized with a Shelly Plus 1 which I directly connected via 230V inside the Heatpump and connected to SG-ready input.


These are the 2 Display screens that shall be condensed into 1 card.
![image](https://github.com/flautze/home_assistant_waterkotte/assets/6823055/c67d2b55-fdb5-4702-9537-f6c0ed1488d9)


![image](https://github.com/flautze/home_assistant_waterkotte/assets/6823055/0af1c1e3-40aa-476c-b940-cc4a7f652b3e)


This is how the Card looks like:

![image](https://github.com/flautze/home_assistant_waterkotte/assets/6823055/ec1dff76-dbaf-4a73-a44a-096327783189)

Functions/features:
- Clicking on the house (top left) -> navigation to a different page/dashboard
- Clicking on the water / heating / cooling icon or temperature -> navigate to a different page/dashboard
- Color of water / heating / cooling changes according to state of the respective enabled and status entities ( running = accent-color, "auto" but not running = primary color, disabled = lightgrey )
- clicking on pump-percentage -> Navigation
- Pump-symbols change color according to state (on = accent-color)
- All the values update according to the sensors and correspond to the layout from the heatpump display
- different graphics (and icon/text-color) for dark/light theme

# How to use
Install the following integration via HACS
https://github.com/marq24/ha-waterkotte

Install the Card-mod Frontend via HACS
https://github.com/thomasloven/lovelace-card-mod

Create a new card on the dashboard, switching to YML-mode.
Copy code from waterkotte.yml and paste.

# Changes required
1. Additional entities
There are several entities that are not originating from the Waterkotte integration. These are marked with comments in the waterkotte.yml
- heatpump_power (center - displaying power consumption of heatpump)
- SG-ready (top right corner)

2. Navigation paths
Navigation paths need to be adjusted according to the dashboard layout, I have not included any sub-pages as these are very basic.

3. Calculated sensors
- Spreizung Heizkreis
- Spreizung Quelle
- Percent Expansion Valve
The sensors can be found in a separate file.

# Additional information
- All icons can be adjusted (in color/size/position) as only the blue/red circulatory system are part of the graphics
- All values can be adjusted in color/size/position
