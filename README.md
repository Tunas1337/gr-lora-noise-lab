## GNU Radio LoRa Noise Lab
![image](https://github.com/user-attachments/assets/b952281b-31e0-4934-9298-a681bf5fa4af)

This repository hosts a GNU Radio flowgraph designed to visually and practically demonstrate the impact of varying noise levels on the integrity of LoRa transmissions and the ability of a receiver to successfully decode the data.
The simulation utilizes the LoRa modulation and demodulation blocks provided by the gr-lora_sdr out-of-tree module, which must be installed separately for this flowgraph to function correctly. Building upon the core LoRa PHY
implementation from gr-lora_sdr, this project integrates channel simulation capabilities, allowing users to introduce controlled amounts of noise and observe the resulting effects on metrics like Bit Error Rate (BER) or
Packet Error Rate (PER), and ultimately, the success or failure of the LoRa demodulation process.

Key features include adjustable parameters directly within the GNU Radio Companion flowgraph, such as noise voltage or Signal-to-Noise Ratio (SNR), enabling straightforward experimentation with different channel conditions.

![image](https://github.com/user-attachments/assets/49da2d19-cf6a-4ebe-bf7a-8f74efa5ce3e)

## Running
To use this flowgraph, first ensure that the dependency gr-lora_sdr, available at https://github.com/tapparelj/gr-lora_sdr/, is properly installed in your GNU Radio environment. Once the dependency is met, you can open the
.grc file included in this repository using GNU Radio Companion, execute the flowgraph, and modify the noise parameters to study how LoRa performance degrades under increasingly challenging channel conditions.

## Difficulties
As per the [open issue](https://github.com/Tunas1337/gr-lora-noise-lab/issues/1), I could not get decoding to work. However, in its current state, the code does allow you to visualize the LoRa modulation chirp spread-spectrum modulation in a couple of ways.

I was also unable to find a good way to visualize the chirps, given the other projects which took up my time. :( This is left for future expansion.
