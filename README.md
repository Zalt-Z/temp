# SafeDrop – Secure File Transfer System

**SafeDrop** is a client-server Python application that securely encrypts, transmits, and stores files with **confidentiality**, **integrity**, and **non-repudiation** using AES, RSA, and digital signatures.

## Features

- **AES-256-CBC** encryption for file confidentiality.
- **RSA-OAEP** to securely encrypt AES keys.
- **RSA-PSS** digital signature for data integrity and sender verification.
- **Base64 encoding** for safe HTTP JSON transmission.
- **Tkinter GUI** for easy user interaction.
- **File dropdown** to select available encrypted files on the server.

## File Structure

SafeDrop/
├── certs/ # Generated RSA key pairs
├── client/
│ └── gui.py # Main GUI application
│ └── crypto.py # Cryptographic logic (encrypt, sign, decrypt, verify)
├── server/
│ └── server.py # Flask server to store and serve encrypted files
│ └── received/ # Folder to store received files
├── generate_keys.py # Script to generate RSA key pairs
├── readme.md

## Setup Instructions

### How to run the server
Perform the following steps on another machine such as a Ubuntu Virtual Machine.

1. Install required Python libraries:
```
pip install flask
```
2. Start the Server:
```
python ./server/server.py
```
Server listens on http://0.0.0.0:5000 and stores encrypted files in received/.


