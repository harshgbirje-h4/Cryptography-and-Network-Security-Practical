# **Experiment 12 — AES Security Analysis: ECB vs CBC**

## **Aim**

To implement AES using ECB and CBC modes, perform encryption and decryption, and analyze repeated plaintext patterns by comparing ciphertext blocks.

## **Requirements**

- Python 3.x
- Visual Studio Code
- Python extension for VS Code
- PyCryptodome

## **Installation**

```bash
python -m pip install -r requirements.txt

Run
python exp12.py
What the program does
Uses AES-128 with a 16-byte key.
Uses repeated plaintext.
Applies PKCS#7 padding.
Encrypts and decrypts using ECB mode.
Displays ECB ciphertext blocks and total/unique block counts.
Generates a random 16-byte IV.
Encrypts and decrypts using CBC mode.
Displays the CBC IV, ciphertext blocks, and total/unique block counts.
Performs a security analysis of ECB vs CBC.
Verifies both decryption results.
Repository Structure
exp12-aes-ecb-vs-cbc/
├── exp12.py
├── requirements.txt
├── .gitignore
├── README.md
└── docs/
    └── exp12.pdf
Notes

CBC output changes between runs because the IV is randomly generated.

The actual number of repeated ECB blocks depends on plaintext alignment with AES's 16-byte block boundaries.

ECB can reveal repeated plaintext patterns when identical plaintext blocks occur at the same block boundaries.

Conclusion

ECB encrypts each block independently and can reveal repeated-block patterns.

CBC uses block chaining and an Initialization Vector (IV), making repeated plaintext patterns less directly visible and providing better confidentiality for structured or repetitive data.