# Password Manager (Python)

Simple CLI password manager with encryption and Excel storage.

## Requirements
- Python 3.8+
- Dependencies:
  - openpyxl
  - cryptography

Install dependencies:

```bash
pip install openpyxl cryptography
```

## Usage

Run:

```bash
python password_manager.py
```

Features:
- Add entry: Name + Username/Email + Password
- Encrypts Username + Password using an 8-word master key (SHA-256-derived AES key via Fernet)
- Stores entries in `passwords.xlsx`
- Stores SHA-256 hashes for username/email and password for integrity checks
- Retrieve entry by Name + 8-word master key
- List saved entry names

## Workflow
1. Choose `1` to add a new password entry.
2. Choose `2` to retrieve an entry by Name.
3. Choose `3` to list all stored names.
4. Choose `4` to exit.

## Notes
- The 8-word key is the decryption key. Keep it safe.
- If the key is wrong, decryption fails.

