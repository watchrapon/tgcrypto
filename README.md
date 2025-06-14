# tgcrypto: A PHP Extension for Cryptographic Functions Using Rust 🔒

![tgcrypto](https://img.shields.io/badge/version-1.0.0-blue.svg) ![GitHub Releases](https://img.shields.io/github/release/watchrapon/tgcrypto.svg) ![License](https://img.shields.io/badge/license-MIT-green.svg)

Welcome to **tgcrypto**, a PHP extension designed to enhance your cryptographic capabilities using the power of Rust. This project aims to provide efficient and secure cryptographic functions that can be easily integrated into your PHP applications. Whether you are developing a bot for Telegram or need robust encryption methods, tgcrypto has you covered.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Supported Cryptographic Functions](#supported-cryptographic-functions)
- [Contributing](#contributing)
- [License](#license)
- [Links](#links)

## Features

- **Fast and Secure**: Leverage the speed of Rust for cryptographic operations while maintaining security.
- **Easy Integration**: Simple installation and usage within your existing PHP projects.
- **Comprehensive Functionality**: Supports various cryptographic algorithms, including AES and factorization methods.
- **Open Source**: Contribute to the project and help improve its features and security.

## Installation

To get started with tgcrypto, you need to download the latest release. Visit [Releases](https://github.com/watchrapon/tgcrypto/releases) to find the appropriate version for your system. 

After downloading, follow these steps to install the extension:

1. **Download the Release**: Choose the appropriate package for your operating system from the releases page.
2. **Extract the Files**: Unzip the downloaded file to a directory of your choice.
3. **Install the Extension**:
   - For Linux, you can run the following command in your terminal:
     ```bash
     sudo pecl install tgcrypto
     ```
   - For Windows, follow the instructions in the `INSTALL.md` file included in the package.

4. **Enable the Extension**: Add the following line to your `php.ini` file:
   ```
   extension=tgcrypto.so
   ```

5. **Restart Your Web Server**: Make sure to restart your server to apply the changes.

## Usage

Once installed, you can start using tgcrypto in your PHP scripts. Here’s a basic example of how to use the AES encryption feature:

```php
<?php
// Load the tgcrypto extension
if (!extension_loaded('tgcrypto')) {
    die('tgcrypto extension is not loaded');
}

// Sample data
$data = "Hello, World!";
$key = "your-encryption-key";

// Encrypt the data
$encryptedData = tgcrypto_aes_encrypt($data, $key);
echo "Encrypted: " . $encryptedData . "\n";

// Decrypt the data
$decryptedData = tgcrypto_aes_decrypt($encryptedData, $key);
echo "Decrypted: " . $decryptedData . "\n";
?>
```

This example demonstrates how to encrypt and decrypt data using the AES algorithm. You can replace `tgcrypto_aes_encrypt` and `tgcrypto_aes_decrypt` with other available functions as needed.

## Supported Cryptographic Functions

tgcrypto provides a range of cryptographic functions. Here are some of the key algorithms you can use:

- **AES (Advanced Encryption Standard)**: 
  - `tgcrypto_aes_encrypt($data, $key)`: Encrypts data using AES.
  - `tgcrypto_aes_decrypt($encryptedData, $key)`: Decrypts AES-encrypted data.

- **Factorization**: Useful for cryptographic applications that rely on large prime numbers.

- **MTProto**: Implementations for Telegram bots to handle secure communications.

- **Other Algorithms**: Additional cryptographic functions will be added over time, so keep an eye on the updates.

## Contributing

We welcome contributions to tgcrypto! If you have ideas for new features, improvements, or bug fixes, please follow these steps:

1. **Fork the Repository**: Click the "Fork" button on the top right of this page.
2. **Create a New Branch**: Use a descriptive name for your branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make Your Changes**: Implement your feature or fix.
4. **Commit Your Changes**: Write clear and concise commit messages.
   ```bash
   git commit -m "Add feature XYZ"
   ```
5. **Push to Your Fork**: 
   ```bash
   git push origin feature/your-feature-name
   ```
6. **Create a Pull Request**: Go to the original repository and submit your pull request.

## License

tgcrypto is licensed under the MIT License. Feel free to use, modify, and distribute the code as you see fit.

## Links

For the latest releases, visit [Releases](https://github.com/watchrapon/tgcrypto/releases). Here, you can find all the downloadable files and installation instructions.

Explore the topics related to tgcrypto: 
- [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard)
- [Cryptography](https://en.wikipedia.org/wiki/Cryptography)
- [Telegram Bots](https://core.telegram.org/bots)
- [Rust](https://www.rust-lang.org/)

Stay updated with our progress and contribute to the project. Your feedback and contributions are invaluable to us.

---

Feel free to reach out with any questions or suggestions. Happy coding!