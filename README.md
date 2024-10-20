# Smart Greenhouse System simulation using Python

This project implements a Smart Greenhouse System simulation using Python and Tkinter for a graphical user interface (GUI). The system is designed to simulate the environmental conditions of a greenhouse, including temperature, light intensity, moisture, and humidity, as well as manage actuators like fans and windows. Users can interact with various settings to control and observe the greenhouse environment over a simulated growth period for crops like strawberries and tomatoes.

![Screenshot 2024-09-03 145105](https://github.com/user-attachments/assets/06d7071d-f8bd-4fcb-aefa-b326ca38bc13)

## Key Features:
- **Real-time Simulation:** The system simulates a controlled environment for plant growth, updating factors like temperature, humidity, and crop growth every second.
- **Interactive Control:** Users can manually adjust key parameters (e.g., temperature, light intensity, soil moisture) through buttons and sliders within the GUI.
- **Automated Sensor Readings:** Simulated sensors provide real-time feedback on environmental conditions like temperature, humidity, and light intensity.
- **Dynamic Plant Images:** Depending on crop growth progress, the system displays updated plant images from a pre-configured set.
- **Actuator Logic:** Automated controls for devices such as heaters, coolers, and humidifiers are toggled based on sensor readings.

## Class Structure:
The system is encapsulated in the `SmartGreenhouse` class, which manages both the UI and the simulation logic. Key attributes include:
- `temperature`, `light_intensity`, `moisture`, and `humidity`: Environmental factors that influence crop growth.
- `window_open`, `fan_on`: Boolean flags representing the state of actuators.
- `simulation_running`: A flag controlling the start/stop status of the simulation.
- `image_folder`: The directory containing plant growth images.

## User Interface Design:
The GUI is organized into two primary tabs:
1. **Settings Tab:** Allows the user to control parameters such as temperature, light, and moisture. It includes radio buttons for plant selection (e.g., strawberries or tomatoes), and buttons to start and stop the simulation.
2. **Additional Settings Tab:** Reserved for future expansions or advanced configurations.

## Simulation Logic:
The system follows a cyclical loop where, for each simulated day, the environment updates based on user inputs and automated logic:
- **Sensor Updates:** Randomized values are generated for temperature, moisture, and light levels.
- **Actuator Controls:** Actuators (heaters, fans, etc.) automatically activate or deactivate depending on the sensor readings.
- **Crop Growth Calculation:** Crop growth is calculated as a percentage over the total simulation days. Once the crop growth reaches 100%, a final image is displayed.

The simulation adjusts the predicted number of days based on environmental factors. If the temperature is too high or moisture too low, crop growth may slow, extending the simulation duration.

## Technical Components:
- **Tkinter Library:** Provides the graphical interface and interaction elements (buttons, sliders, labels).
- **Random Library:** Used to simulate the unpredictable aspects of real greenhouse conditions such as fluctuations in temperature and moisture.
- **PIL (Pillow):** Handles image loading and updates for crop growth progression.
