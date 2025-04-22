# instrumentation-amplifier
# Theory:
An instrumentation amplifier is a type of differential amplifier designed to amplify very small differential signals while rejecting large common-mode voltages (like noise or interference). It's commonly used in applications like sensor data acquisition, biomedical measurements (like ECG or EEG), and industrial monitoring.
Key Features:
High input impedance: Doesn’t load the signal source.
High common-mode rejection ratio (CMRR): Great at ignoring noise that affects both inputs equally.
Adjustable gain: Easy to set using a single resistor (in typical 3-op-amp configurations).
Low output impedance: Can drive loads or connect to ADCs effectively.
Basic 3-Op-Amp Instrumentation Amplifier Structure:
First Stage (Buffering & Gain):
Two op-amps buffer the inputs and provide initial gain.
This stage ensures high input impedance.
Second Stage (Differential Amplifier):
Subtracts the outputs of the first stage.
Final amplified differential signal is produced here.
Gain Formula (3-Op-Amp Version):
Gain=1+ 
  is the gain-setting resistor between the two buffer op-amps.
Applications:
Strain gauge signal amplification
Temperature sensors (RTDs, thermocouples)
ECG, EEG, EMG biomedical sensors
Industrial control systems
typically, it consists of three operational amplifiers in a specific configuration: two op-amps in the first stage act as buffers with gain, while the third op-amp in the second stage functions as a differential amplifier. The gain of the instrumentation amplifier can be easily adjusted by changing a single external resistor, allowing for flexible amplification settings. Because of its accuracy and stability, the instrumentation amplifier is widely used in applications such as biomedical signal processing (e.g., ECG, EEG), sensor interfacing, and industrial process control, where small and sensitive signals need to be measured reliably in noisy environments.

# Design question:
Design an instrumentation amplifier using 3 op-amps configuration with the following constraints.

R1=R2=R3=R4=R5=R6=100kΩ
Difference gain Adm=20v/v
Find Acm and calculate CMRR for Adm=20v/v and 50v/v, by using LT spice simulator.

# Calculations:
for Adm=20v/v
Rg=[20000/19] =10.5kΩ

For Adm=50v/v
Rg=[20000/49] =4.08kΩ

 # Circuit Diagram:
for Adm=20v/v
![1](https://github.com/user-attachments/assets/d43ebe11-8ac6-44a2-a26c-ba8d8dea62f4)
# Output
![10 5k with common mode volage](https://github.com/user-attachments/assets/dbdeb103-e3c0-49b7-8b71-164183a56b97)
for Adm = 50v/v
# Circuit diagram






