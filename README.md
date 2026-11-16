# fl2k_amp
3-channel adjustable gain amplifier board for https://github.com/osmocom/osmo-fl2k (Fresco Logic FL2000 USB 3.0 to VGA DAC)

When using an FL2000 dongle for baseband video generation (such as NTSC/PAL CVBS composite video, S-Video Y/C, RGB/YPbPr component video), the raw R/G/B current-steering DAC outputs have limited drive capability and non-adjustable full-scale swing (~0.7 Vpp into 75Ω). fl2k_amp provides proper 75Ω input termination, high-bandwidth amplification with per-channel trimmer gain control, low-noise linear power regulation, and 75Ω source-terminated BNC coaxial outputs.

Power supply: 3xAA batteries in series or 5V USB.

Replace R4, R5, R6 with 500 Ω resistors, or use two 1 kΩ resistors in parallel (stack soldering) for further gain boost.

100ire_ntsc_16fsc.s8 is a calibration file. It contains 8-bit signed composite video sampled at 16fsc (630/11 MHz), representing a 100 IRE white level. Calibrate this signal to achieve a 1 V peak-to-peak amplitude under a 75 Ω load.
