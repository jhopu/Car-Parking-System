# Car Parking Safety Circuit Using Infrared Sensor

## Overview
This project aims to develop a Car Parking Guard Circuit that alerts the driver when an obstacle is detected behind the car at a specific distance. The system provides both auditory and visual warnings to help the driver avoid potential collisions.

## Key Components
- **IR Transmitter and Receiver**: Detects obstacles by emitting and receiving infrared rays.
- **555 Timer**: Generates pulse waveforms for controlling various circuit elements.
- **JK Flip-Flop**: Used in the frequency divider circuit to reduce signal frequency.
- **Multiplexer**: Handles the selection of different frequencies for the piezo-buzzer based on obstacle proximity.
- **Comparators (LM324)**: Used to segment the distance measurement range and control LED indicators.
- **XOR Gate (7486 IC)**: Utilized in the frequency selection logic.
- **Piezo Buzzer**: Emits sound based on the selected frequency to alert the driver.

## Sections

### 1. IR Transmitter-Receiver
The IR sensor detects obstacles within a specific range. The circuit employs two IR transmitters and one IR receiver, which can measure distances up to 25 cm. The output voltage of the IR receiver varies with distance, allowing the circuit to determine proximity to obstacles.

### 2. Thresholding Circuit
This circuit uses LM324 comparators to establish thresholds for different distance ranges. Each comparator corresponds to a specific distance, triggering different LED indicators (Green, Yellow, Red) based on proximity.

### 3. Pulse Generator Circuit
A 555 Timer is used to generate pulse waveforms with a specific frequency to activate the piezo-buzzer. The frequency of the waveform is determined by the values of the resistors and capacitors in the circuit.

### 4. Frequency Divider Circuit
The frequency divider circuit, built using JK flip-flops, reduces the input signal frequency. The circuit divides the frequency by 2 in each stage, ultimately producing an output frequency that is a fraction of the original signal.

### 5. Frequency Selection Circuit
This circuit adjusts the operating frequency of the piezo-buzzer based on the distance measured by the IR sensor. A multiplexer is used to select between different frequencies, making the buzzer sound more frequently as the obstacle gets closer. The selection signals are generated using the output from the comparators.

### 6. Observations and Results
The circuit successfully detects obstacles within a 25 cm range and triggers the corresponding LED indicators and piezo-buzzer based on proximity. The system provides accurate and timely alerts to the driver, enhancing parking safety.

## Conclusion
This Car Parking Safety Circuit is a cost-effective solution to prevent collisions while parking. By detecting obstacles and providing both visual and auditory alerts, it helps drivers maneuver safely in tight spaces.
