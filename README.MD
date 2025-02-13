# inkjetDriver

An exploration of driving inkjets using minimal boards and hardware

## Table of Contents

- [Research](#research)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Research

Two major different types of inkjet:

a) thermal - benefit to trying many different materials as drivers/cartridges are disposable

b) piezo - better for diversity of materials as no change of phase is needed.

They both have their pros and cons, both systems generally struggle with higher viscosities.

Annoyingly they all have their own driver requirements, some inkjet heads have built in drivers and use shift register driven strings to receive commands, others provide direct access to the dispense nozzles.

Past projects
- Epson
    - issue: proprietary drivers trigger methods
    - issue: can't do viscous reagents
- [Xaar 128](https://github.com/gkyle/xaar128?tab=readme-ov-file)
    - issue: exposed traces, no aqueous options
- [HP C6602](https://github.com/NicholasCLewis/InkShield)
    - issue: thermal inkjets could damage or react poorly with media
    - issue: 96 dpi is a bit low
- [HP45](https://ytec3d.com/hp45-controller-v4/)
    - issue: some complexity with repurposing this design as the DMA is used
    - issue: thermal inkjets could damage or react poorly with media

I think the HP45 is a great solution overall as the DPI is relatively high (up to 600dpi!), but this might play havoc with some of the desired media. Ultimately, we may have to go piezo jet.

For this project I've selected the [Spectra 512](https://asset.fujifilm.com/www/nl/files/2020-06/ef42a0951e1e88574ddcf7afa8dcb755/PDS00070.pdf) by Dimatix/Fujifilm, an [MP108FD amplifier](https://www.apexanalog.com/resources/products/mp108u.pdf) from Apex Microtechnologies, and a [Teensy 4.1](https://www.pjrc.com/store/teensy41.html) to control everything and provide waveforms.

## Usage

Explain how to use the project or provide examples.

## Contributing

Describe how others can contribute to the project.

## License

This project is licensed under the [License Name] - see the [LICENSE.md](LICENSE.md) file for details.