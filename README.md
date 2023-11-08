# Waterkotte Display using the pictures entity card
This Repository was created to share the setup of the pictures entity card to emulate/imitate the Waterkotte heatpump display overview.
All the sensors used are coming from the Waterkotte Integration: 

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
- heatpump_power
- SG-ready

2. Navigation paths
Navigation paths need to be adjusted according to the dashboard layout.

3. Calculated sensors
- Spreizung Heizkreis
- Spreizung Quelle
- Percent Expansion Valve
The sensors can be found in a separate file.
