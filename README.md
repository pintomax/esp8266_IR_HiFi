# This is Python virtual env folder for latest ESPHome version 2026.1.5, Home Assistant version 2026.1.2

# Use Espressif ESP8266 nodecmd 12E

# Ubuntu 24 LTS

# 1 create virtual env (venv)

python3 -m venv ./venv

# 2 activate it
source venv/bin/activate

# 3 connect:
- Infrared LED to ESP8266 pin D5 and place it close or internally to HiFi case
- Binary sensor to pin D7 detecting 12V to subwoofer relay box is active
- Relay switch uses pin D6 for activating subwoofer (220v) via relay (12V)
- Connect neopixel RGB LED to pin D8 (9 LEDS for this setup)
- Connect another neopixel RGB LED to pin D3 (12 LEDs) for VU-meter effect
- Connect tranformer to ADC pin for sound level acquisition
- Use an ol AC volage transformer (say 220 V to 12 V AC) and remove secondary windings, then use primary windings connected to GND and ADC
  Use 3 or 5 turns of the loudspeaker cable (R+ or R- or L+ or L-) in the place of secondary windinga.

# 4 set WiFi network and password aliong with encryption key

# 5 compile and upload via USB

esphome run hifi.yaml

# 6 check Home Assistant for a new ESPHome device and connect by using the encryption key in hifi.yaml

