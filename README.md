# meteor-m2-4-cf32-dataset
A dataset of Meteor-M2-4 satellite LRPT signal recordings captured as CF32/IQ files, along with their corresponding decoded ZIP and RAW image products for analysis, signal processing, and satellite reception research.
# Meteor-M2-4 LRPT SDR Dataset

A collection of Meteor-M2-4 satellite LRPT signal recordings captured using an SDR-based ground station, together with the corresponding decoded image products.
The dataset is intended for experimentation with satellite signal reception, SDR, digital signal processing, LRPT decoding, and satellite imagery reconstruction.

# Dataset Overview

# Each observation contains:

A raw CF32 complex IQ recording captured from the Meteor-M2-4 LRPT transmission.
The corresponding decoded image/product files generated from the received signal.
Supporting metadata where available.

The raw recordings and decoded products are provided together so that the complete chain from received RF signal → digital samples → decoded satellite imagery can be studied.

# Satellite Information

Satellite: Meteor-M2-4
Mission: Meteor-M2 series weather satellite
Signal: LRPT (Low Rate Picture Transmission)
Reception: SDR-based ground station

# Repository Structure
meteor-m2-4-sdr-dataset/
├── README.md
├── metadata/
├── cf32/
│   ├── pass_001.cf32
│   ├── pass_002.cf32
│   └── ...
├── decoded/
│   ├── pass_001.zip
│   ├── pass_001.raw
│   └── ...
└── LICENSE

The exact directory structure may change as additional recordings are added.

Data Types
CF32

The .cf32 files contain the raw complex baseband/IQ samples captured during Meteor-M2-4 reception.

CF32 generally represents 32-bit floating-point complex samples, with the real and imaginary components representing the I/Q signal.

These files can be used for:

Signal inspection
Spectrum analysis
Demodulation experiments
LRPT decoding
DSP research
Reproducibility of the reception process
Decoded Products

The corresponding decoded files contain products generated from the received LRPT signal.

Depending on the recording, these may include:

.zip products
.raw image/data files
Other decoder-generated products

The decoded products provide a reference for comparing the original received signal with the final reconstructed imagery.

# Recording → Decoded Product Mapping

Where possible, each recording follows a common identifier:

pass_001.cf32
        │
        └── decoded/pass_001/
              ├── product.zip
              └── product.raw

This allows the raw signal recording to be associated with its corresponding decoded output.

# Potential Uses

This dataset can be useful for:

Meteor-M2-4 LRPT reception experiments
Software-defined radio (SDR) research
Digital signal processing
Satellite communication studies
LRPT decoder development and testing
Raw IQ signal analysis
Satellite image reconstruction
Machine-learning datasets for signal processing
Reproducible satellite reception experiments

# Tools
The recordings and products can be analyzed using SDR and satellite-reception software such as:

SatDump
GNU Radio
SDR++
MATLAB
Python-based DSP tools

The decoded products in this repository can also be used to verify the output of an independent decoding pipeline.

# Important Notes
The CF32 files are raw signal recordings and may be large.
Recording parameters such as sample rate, center frequency, gain, antenna configuration, and reception time may vary between observations.
Metadata should be consulted before comparing recordings.
The decoded products are provided as corresponding reference outputs where available.
This repository is intended for research, experimentation, education, and reproducibility.

# Contribution
Additional Meteor-M2-4 recordings and corresponding decoded products can be contributed to the dataset.

When adding a new observation, please provide as much metadata as possible, including:

Reception date and time (UTC)
Center frequency
Sample rate
SDR hardware
Antenna
Gain settings
Maximum elevation
Recording duration
Decoder/software used
Decoding status

# License
The licensing terms for the recordings and decoded products should be specified here according to their intended distribution and ownership.

# Acknowledgements

Meteor-M2-4 is part of the Meteor-M series of meteorological satellites. This dataset contains ground-station reception data captured for experimental and educational purposes.


