# VL.AxiDraw

A vvvv gamma patch and workflow to control pen plotters (e.g. AxiDraw and IDraw) directly from within the visual programming environment - no need for Inkscape or other intermediary tools.

This library simplifies the plotting workflow by allowing users to:

* Load `.svg` files in vvvv
* Configure runtime parameters such as pen speed, port, and file path
* Send plot commands directly via the command line
* Optionally receive WhatsApp notifications when plotting is complete

It provides a faster, more customizable workflow for generative or procedural plotting directly from vvvv gamma.

## Wrapper Dependencies

This patch uses the open-source **AxiDraw CLI** by Evil Mad Scientist.
Version used: [AxiDraw CLI v1.0.1](https://axidraw.com/doc/cli_api/#introduction)

## Supported Devices

* [AxiDraw Pen Plotters](https://axidraw.com/)
* [IDraw Pen Plotters](https://www.idrawpenplotter.com/)

For IDraw plotters, some additional configuration steps are required (see below).

## Requirements

### Dependencies

* [vvvv gamma](https://visualprogramming.net) (2023.5+ recommended)
* [Python 3.10+](https://www.python.org/downloads/)
* [AxiDraw CLI](https://axidraw.com/doc/cli_api/#introduction)

### Optional Integration

* [Call Me Bot](https://www.callmebot.com/) - to receive WhatsApp notifications when the plot finishes

## Getting Started

### 1. Install Python and AxiDraw CLI

Follow instructions here: [https://axidraw.com/doc/cli\_api/#introduction](https://axidraw.com/doc/cli_api/#introduction)

### 2. Prepare Configuration File

Locate:

```
C:\Users\[YourName]\AppData\Local\Programs\Python\Python313\Lib\site-packages\axidrawinternal\axidraw_conf.py
```

Copy it to your working directory. Do not modify the original.

### 3. Adjust for IDraw Plotters (if needed)

* Scale your SVGs up by **25%** 
* Adjust plot area size (25% larger than A3, in inches) in the config file
* Swap `PenUp` and `PenDown` values in config file

### 4. Load Patch and Configure Runtime Settings

Use the exposed I/O boxes to:

* Set file path
* Define pen positions and plot area
* Enable/disable WhatsApp notifications
* speed and pen positions

These settings override the static config file.

## Limitations

* This is a patch-based tool, not a compiled library
* IDraw support requires manual config changes and scaling

## For Use With

[vvvv gamma](https://vvvv.org) - the visual live-programming environment for .NET

## Credits

* Based on [AxiDraw CLI](https://github.com/evil-mad/AxiDraw) by Evil Mad Scientist
* Thanks to [Call Me Bot](https://www.callmebot.com/) for the WhatsApp integration service

## Sponsoring

Development of this library was partially supported by:

* [Flow Architecture](https://flowarchitecture.co.uk)