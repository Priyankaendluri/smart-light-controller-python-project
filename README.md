# smart-light-controller-python-projimport time
import random

# Threshold for darkness detection
LIGHT_THRESHOLD = 30  # 0 = dark, 100 = very bright

# Function to simulate reading from a light sensor
def read_light_sensor():
    # Simulate light sensor with random values (replace with actual sensor reading)
    return random.randint(0, 100)

# Function to control the light
def control_light(light_level):
    if light_level < LIGHT_THRESHOLD:
        return "ON"
    else:
        return "OFF"

# Main loop
try:
    while True:
        light_level = read_light_sensor()
        light_state = control_light(light_level)

        print(f"Light Level: {light_level} | Light State: {light_state}")

        # Wait 1 second before checking again
        time.sleep(1)

except KeyboardInterrupt:
    print("\nSmart Light Controller stopped.")ect