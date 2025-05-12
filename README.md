# 🔐 RSA Encryption & Decryption GUI Tool

A modern Python GUI application that performs RSA encryption and decryption of text and files. It provides a user-friendly interface for securely encoding messages using asymmetric cryptography.

---

## 📘 What is RSA?

RSA (Rivest–Shamir–Adleman) is one of the first public-key cryptosystems and is widely used for secure data transmission. Unlike symmetric encryption, RSA uses **two keys**:
- A **public key** for encryption
- A **private key** for decryption

RSA is based on the computational difficulty of factoring large prime numbers, making it highly secure when large key sizes are used.

---

## 👨‍🔬 Who Invented RSA?

RSA was invented in **1977** by:
- **Ron Rivest**
- **Adi Shamir**
- **Leonard Adleman**

They introduced RSA as a public-key cryptosystem that enables secure communication even over insecure networks.

---

## ⚙️ How RSA Works (In Simple Steps)

1. **Key Generation**:
   - Select two large prime numbers `p` and `q`
   - Compute `n = p * q`
   - Calculate Euler’s totient function: `ϕ(n) = (p-1)(q-1)`
   - Choose an encryption exponent `e` such that `1 < e < ϕ(n)` and `gcd(e, ϕ(n)) = 1`
   - Compute the decryption exponent `d` such that `(d * e) % ϕ(n) = 1`

2. **Encryption**:
   - Cipher = (Plaintext<sup>e</sup>) mod n

3. **Decryption**:
   - Plaintext = (Cipher<sup>d</sup>) mod n

The public key is `(e, n)` and the private key is `(d, n)`.

---

## 💻 How This Project Works

### Core Functionalities

- 🔐 **Generate Keys**: RSA key pairs are generated and can be saved as `.json`
- ✍️ **Encrypt Text**: Encrypt any user input or text file using the public key
- 🔓 **Decrypt Text**: Decrypt RSA-encrypted messages with the private key
- 💾 **Save & Load Keys**: Store and load key pairs securely
- 📂 **File Encryption/Decryption**: Supports `.txt` and `.enc` file formats
- ⚠️ **Error Handling**: Provides alerts for missing or incorrect keys

---

## 🎨 GUI Design

Built using **Python’s `tkinter` and `ttk` libraries**, the interface features:
- Clean layout with modern styling
- Separate sections for plaintext, encrypted, and decrypted output
- Buttons for all key actions
- Error dialogs and helpful prompts

---

## 📦 Project Structure

```bash
rsa-encryption-gui/
│
├── rsa_gui.py         # Main GUI Application
├── rsa_core.py        # Encryption, decryption, and key logic
├── rsa_keys.json      # Sample RSA key file (generated on save)
├── TEST1.txt          # Sample input file for testing
└── README.md          # Project documentation
```

## 🧪 Features in Action
Generate RSA key pair

Enter text to encrypt

Click Encrypt to view the encrypted message

Click Decrypt to restore the original message

Use File Encrypt/Decrypt for .txt and .enc files

Save and load keys for reuse

---

## 🔒 Security Note
Always protect your private key

Use longer key sizes (1024+ bits) for real-world applications

This project is educational — for serious applications, use established libraries like cryptography or PyCryptodome

---

## 📜 License
This project is licensed under the MIT License – free to use and modify.

---

## 👨‍💻 Author
K. Sai Abhiram,
Undergrad Student,
VIT-AP University.

## 🚀 Empower your messages with RSA — because real security starts with smart encryption. 🔐
