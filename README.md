# NOAA ITOS HRPT decoder

*Many thanks to Ryzerth from [SDR++](http://sdrpp.org) for his invaluable help*

A simple GNU Radio based flowgraph to decode ITOS HRPT (e.g from NOAA-2).

Documentation on [my website](https://www.a-centauri.com/articoli/noaa2-satellite-reception)

Additional info on the [SigID Wiki](https://www.sigidwiki.com/wiki/NOAA_ITOS_High_Resolution_Picture_Transmission_(HRPT))

A baseband for testing purposes is available in this repository (NOAA2.wav), but you only need the `ITOS_Decoder.grc` file if you have your own baseband.

## Usage

Open the file with GNU Radio. Adjust the path of the file in the `Wav File Source` block and the `wav_samp_rate_mhz` variable with the sample rate of the file, **in MHz** (e.g. 4 for 4 MHz).
Start the decode, it should produce some calibration ramp in the raster.
If the image is slanted, adjust `samples_per_line` slowly until the image is perfectly straight.
