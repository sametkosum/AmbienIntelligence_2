# Ambient Intelligence Project: Ground Regulation at Camp Nou Stadium
The current ontology represents vertical farming examply for Ambient intelligence exercise II. The application is built using [Protegé](https://protege.stanford.edu/) software. 

## Project Overview

Welcome to the Ambient Intelligence project for optimizing the environment at Camp Nou Stadium based on grass and weather conditions. This system utilizes smart sensors to monitor real-time data and dynamically regulate the stadium environment. The project aims to provide a comfortable, safe, and sustainable experience for visitors.

## Project Objective

The primary goal of this project is to introduce an Ambient Intelligence system that optimizes the environment at Camp Nou Stadium by monitoring grass and weather conditions. The system responds dynamically to ensure the optimal grass level, providing adaptive and effective measures based on specific weather and grass conditions.
**Author**: *[Ahmet Samet Kosum](https://github.com/sametkosum)*, [s56358306@studenti.unige.it](s5635830@studenti.unige.it)

**Course Instructors**: *[Antonio Sgorbissa](https://rubrica.unige.it/personale/UkNHWlJp)*


## Benefits to Users

1. **Comfort and Enjoyable Experience:**
   - *Optimized Environment:* Continuous monitoring of grass and weather conditions ensures an optimized environment for stadium events.
   - *Personalized Control:* Users can customize environmental conditions through a mobile application, enhancing their comfort.

2. **Safety and Health:**
   - *Optimal Grass Condition:* Intelligent interventions ensure the grass is always in optimal condition, prioritizing user safety.
   - *Weather Alerts:* The system provides alerts about changing weather conditions, enabling visitors to prepare for outdoor activities.

3. **Environmental Sustainability:**
   - *Energy Efficiency:* Minimizing the energy consumption of systems supports environmental sustainability.
   - *Optimized Resource Usage:* Efficient use of resources such as water and energy promotes sustainable stadium operation.

## Ambient Intelligence Aspects

1. **Real-time Data Processing and Analytics:**
   - *Instant Decision-Making:* Continuous data processing enables the system to make instant decisions based on smart sensor inputs.
   - *Predictive Models:* Predictive models help forecast future grass and weather conditions, facilitating effective interventions.

2. **Dynamic System Adaptation:**
   - *Adaptation to Variable Conditions:* Smart sensors allow the system to dynamically adapt to changing conditions for continuous effectiveness.
   - *Smart Adjustments:* The system can adapt individually to users, adjusting environmental conditions based on preferences.

## Classes and Subclasses

- **Thing**
  - **SmartFootballStadium**
    - **GrassCondition**
      - WetGrass
      - DryGrass
      - SnowCoveredGrass
    - **WeatherCondition**
      - ColdWeather
      - NormalWeather
      - HotWeather
    - **TemperatureCondition**
      - HighTemperature
      - LowTemperature
    - **Sensor**
      - GrassSensor
      - WeatherSensor
      - TemperatureSensor
    - **RegulationDevice**
      - HeaterSystem
      - WaterGridSystem
      - IrrigationSystem

## Object Properties

1. **hasCondition**
   - *Domain:* SmartFootballStadium
   - *Range:* GrassCondition, WeatherCondition, TemperatureCondition
   - *Description:* Relates the stadium to its current conditions.

2. **usesSensor**
   - *Domain:* SmartFootballStadium
   - *Range:* Sensor
   - *Description:* Relates the stadium to the sensors it uses.

3. **regulatesWithDevice**
   - *Domain:* SmartFootballStadium
   - *Range:* RegulationDevice
   - *Description:* Relates the stadium to the devices it uses for regulation.

4. **isConnectedTo**
   - *Domain:* GrassCondition, WeatherCondition, TemperatureCondition
   - *Range:* GrassCondition, WeatherCondition, TemperatureCondition
   - *Description:* Indicates the relationships between different conditions.

## Data Properties

1. **hasTemperatureValue**
   - *Domain:* TemperatureSensor
   - *Range:* xsd:float
   - *Description:* Represents the temperature value obtained from the sensor.

2. **hasWeatherType**
   - *Domain:* WeatherSensor
   - *Range:* xsd:string
   - *Description:* Represents the type of weather condition obtained from the sensor.

3. **hasGrassStatus**
   - *Domain:* GrassSensor
   - *Range:* xsd:string
   - *Description:* Represents the status of the grass obtained from the sensor.

4. **regulationStatus**
   - *Domain:* RegulationDevice
   - *Range:* xsd:string
   - *Description:* Represents the status of the regulation device (on/off, active/inactive).

5. **hasSystemStatus**
   - *Domain:* RegulationDevice (IrrigationSystem, HeaterSystem, WaterGridSystem)
   - *Range:* xsd:string    
