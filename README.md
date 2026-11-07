# reconstruct-FileSignatureScanner
Scans a file and identifies the file type based on its signature, even if the file extension is incorrect or missing. Uses a pre-defined or user-provided signature database. When a custom database is supplied and no custom signature matches, identification falls back to python-magic. A target file that does not exist, and a file whose type cannot be identified, both end the run with exit code 1 and distinct messages. The extraction output path (-o) must not be the scanned file itself; such a run is refused with exit code 1. - Focused on Tools for attempting to recover usable files or data from fragmented or corrupted data sources. Focuses on file type identification and partial data extraction, often from disk images or memory dumps.

## Install
`git clone https://github.com/ShadowGuard-AI/reconstruct-filesignaturescanner`

## Usage
`python3 main.py file_path [-d DATABASE] [-e] [-o OUTPUT]`

## Parameters
- `file_path` (required): Path to the file to scan.
- `-h, --help`: Show help message and exit
- `-d, --database`: Path to a custom signature database (JSON). If no custom signature matches, identification falls back to python-magic.
- `-e, --extract`: Attempt data extraction based on identified file type.
- `-o, --output`: Path to save extracted data.

## License
MIT License. See LICENSE.
