This project involves in low-amplitude signal-synchronization.
While traditional definition of synchronization is aligning the phase, my project involves in preserving the signal's integrity and letting the signals pass to the backend device together.
Amplitude threshold is 0.2V.
Allows both analog and digital signal to be synchronized.
The signal integrity matters for fields where all the signals need to be present and the original phase relationship between each others matters.
Some application fields include: Medical, Industrial, and Automotive.
Medical: Allows ECG signals (already amplified ECG signals) to be gated and pass to the simultaneous ADC at the same time, allowing the ADC and backend controllers to perform task when all the signals are present.
This reduces power consumption, computational resources consumption. Then, the performance and real-time responsiveness of the device using my method can improve.
Industrial: Similar logic as medical. Application examples include analog mems accelerometer and similar sensor systems.
Automotive: Similar logic as medical. Application examples include throttle systems and similar sensor systems.
Important note: This method can be applied in redundant sensor or multi-sensor systems that require the original signal's integrity.
Some information before all signals may lost in certain applications. The user should decide by themselves whether the lost part of the signal matters.
If the computation of input signals in any application is based on the entire signal, the user should consider the trade-off using my method.
If the computation of input signals in any application is based on only the signal after all signals arrive, my method is applicable. More testing and refinement should always be implemented for better usage.
If the user wants a higher bandwidth, please use high-bandwidth MOSFET and OP-AMP and upgrade any other components if needed.
The method itself does not have a frequency threshold. The components limits the bandwidth.
This is the schematic: <img width="1279" height="715" alt="image" src="https://github.com/user-attachments/assets/68f06d6f-8984-4be8-a3b1-4de9b0562720" />
