# reconstruct-FileSignatureScanner
Scans a file and identifies the file type based on its signature, even if the file extension is incorrect or missing. Uses a pre-defined or user-provided signature database. When a custom database is supplied and no custom signature matches, identification falls back to python-magic. A target file that does not exist, and a file whose type cannot be identified, both end the run with exit code 1 and distinct messages. The extraction output path (-o) must not be the scanned file itself; such a run is refused with exit code 1. - Focused on Tools for attempting to recover usable files or data from fragmented or corrupted data sources. Focuses on file type identification and partial data extraction, often from disk images or memory dumps.

## Install
`git clone https://github.com/ShadowStrikeHQ/reconstruct-filesignaturescanner`

## Usage
`./reconstruct-filesignaturescanner [params]`

## Parameters
- `-h`: Show help message and exit
- `-d`: Path to a custom signature database (JSON). If no custom signature matches, identification falls back to python-magic.
- `-e`: Attempt data extraction based on identified file type.
- `-o`: Path to save extracted data.

## License
Copyright (c) ShadowStrikeHQ
