hu# instrumentation-amplifier
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
![2](https://github.com/user-attachments/assets/286d5b72-75b2-4b90-bd07-3abaa912ff26)

# Output
![10 5k with common mode volage](https://github.com/user-attachments/assets/dbdeb103-e3c0-49b7-8b71-164183a56b97)
 # for Adm = 50v/v
# Circuit diagram
![1](https://github.com/user-attachments/assets/ed38e202-5405-40c1-a35d-bde139705e50)
Output
![4 08k with common mode voltage ckt](https://github.com/user-attachments/assets/c087d0f1-1ee6-4d86-9ac3-756035019cca)

from above output we get vout=0.9*10^-9
Acm=vout/vin
Acm=9*10^-9
CMRR=20log(Adm/Acm)
CMRR=194.8dB
# Result 
  A voltage graph or measured output showing the amplified difference between the two inputs. Let me know if you're simulating and want help analyzing that
see 𝑉out rising, oscillating, or behaving based on the differential input.
Useful for checking gain, linearity, and signal response.

# Inference
High Gain Accuracy:
The output voltage closely matches the theoretical gain formula
Excellent Common-Mode Rejection (CMRR):
When the same signal is applied to both inputs the output remains near zero. 
Output voltage increases linearly with increasing differential input voltage.
 Confirms that the amplifier maintains good linearity, essential for accurate signal measurement.
Stable Frequency Response:
From AC analysis, the gain remains constant over a desired frequency range, then drops off after a certain point (cutoff frequency).
✅Suitable for applications like biomedical signals or low-frequency sensors.
Noise and Offset Minimization:
Small input differences (e.g., 10 mV) produce a clear output without significant noise or offset (assuming ideal or precision op-amps).
 Demonstrates the amplifier’s sensitivity and precision
The LTspice simulation validates that the instrumentation amplifier:
Correctly amplifies differential signals
Suppresses common-mode noise
Delivers linear and accurate outputIs suitable for precise, low-level signal applications








