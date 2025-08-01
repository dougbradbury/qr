# QR Code Generator

A simple command line tool for generating QR codes.

## Setup

The project includes a Python virtual environment with all dependencies installed.

To activate the environment:
```bash
source qr_env/bin/activate
```

## Usage

Basic usage:
```bash
python qr "https://example.com"
```

### Options

- `-o, --output`: Output filename (default: qr_code.png)
- `-s, --size`: Box size (default: 10)
- `-b, --border`: Border size (default: 4)
- `-e, --error-correction`: Error correction level L/M/Q/H (default: L)
- `--fill-color`: Fill color (default: black)
- `--back-color`: Background color (default: white)

### Examples

```bash
# Generate QR code with custom filename
python qr "https://psbs.printful.me/" -o printful_qr.png

# Large QR code with high error correction
python qr "https://example.com" -s 15 -e H -o large_qr.png

# Custom colors
python qr "Your text here" --fill-color blue --back-color yellow
```

## Dependencies

- Python 3.x
- qrcode[pil] 8.2
- pillow 11.3.0

## Installation

If you need to recreate the environment:
```bash
python -m venv qr_env
source qr_env/bin/activate
pip install qrcode[pil] pillow
```