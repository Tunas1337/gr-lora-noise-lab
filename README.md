This repository hosts a GNU Radio flowgraph designed to visually and practically demonstrate the impact of varying noise levels on the integrity of LoRa transmissions and the ability of a receiver to successfully decode the data.
The simulation utilizes the LoRa modulation and demodulation blocks provided by the gr-lora_sdr out-of-tree module, which must be installed separately for this flowgraph to function correctly. Building upon the core LoRa PHY
implementation from gr-lora_sdr, this project integrates channel simulation capabilities, allowing users to introduce controlled amounts of noise and observe the resulting effects on metrics like Bit Error Rate (BER) or
Packet Error Rate (PER), and ultimately, the success or failure of the LoRa demodulation process.

Key features include adjustable parameters directly within the GNU Radio Companion flowgraph, such as noise voltage or Signal-to-Noise Ratio (SNR), enabling straightforward experimentation with different channel conditions.
To use this flowgraph, first ensure that the dependency gr-lora_sdr, available at https://github.com/tapparelj/gr-lora_sdr/, is properly installed in your GNU Radio environment. Once the dependency is met, you can open the
.grc file included in this repository using GNU Radio Companion, execute the flowgraph, and modify the noise parameters to study how LoRa performance degrades under increasingly challenging channel conditions.
