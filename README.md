# JBScrape

Find jailbreakable iPhones on eBay and Swappa.

Searches for devices running **iOS 16.0-16.6.1** and **iOS 17.0**.

## Features

- Searches eBay and Swappa for iPhones with jailbreakable iOS versions
- Filters out impossible device/iOS combinations (e.g., iPhone 4 claiming iOS 16)
- Only checks seller descriptions on Swappa (ignores buyer comments asking about iOS)
- Organizes results by device model and price
- Exports to JSON and optionally creates a note in macOS Notes app

## Requirements

- Python 3.8+
- Google Chrome browser

## Installation

```bash
# Clone the repo and enter the directory
git clone https://github.com/zeroxjf/JBScrape.git
cd JBScrape

# Create and activate virtual environment (recommended)
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

## Usage

```bash
python JBScrape.py
```

## How It Works

1. **eBay**: Searches for listings mentioning specific iOS versions in titles
2. **Swappa**: Visits individual listings and checks seller descriptions only (not buyer Q&A comments)
3. **Validation**: Filters out impossible combinations (e.g., old devices claiming new iOS)
4. **Output**: Groups results by device model, sorted by price

## License

MIT License - see [LICENSE](LICENSE)
