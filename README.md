# Secrets Handbook

A comprehensive guide for securely storing sensitive information such as cryptocurrency seed phrases and root passwords.

## Overview

This handbook provides a security-focused approach to storing critical secrets that:
- Protects cryptocurrency seed phrases for self-custody wallets
- Secures sensitive text information even when stored in cloud services
- Creates an encrypted backup system for vital credentials

## Prerequisites

You'll need the following tools:
- [BIP39 Tool](https://github.com/iancoleman/bip39/releases) - Download `bip39-standalone.html`
- [Symmetro](https://github.com/neutronstar03/symmetro/releases) - Download `symmetro-v2.0.0.html` (or newer version)
- [Rabby Wallet](https://rabby.io/) (recommended browser extension, install only - don't configure yet)
- Optional: [AirGap](https://airgap.it/) on a smartphone for cold storage
- A memorable password that you will never write down (stored only in your memory)

## Security Process

### Step 1: Prepare Your Environment

1. Boot your device in safe mode:

   **Windows 10/11:**
   - Press `Windows + R`
   - Type `msconfig` and click `OK`
   - Select the `Boot` tab
   - Check `Safe boot` option
   - Click `Apply` and close
   - Restart when prompted (or restart manually)

   **Ubuntu:** - If you have an improvement suggestions, please go into [Pull Requests](https://github.com/neutronstar03/secrets-handbook/pulls)
   - Restart your computer
   - When the GRUB menu appears, select "Advanced options for Ubuntu"
   - Select the recovery mode option (usually shows as "Ubuntu ... (recovery mode)")
   - From the recovery menu, select "root" to get a root shell
   - Mount the filesystem as read-write: `mount -o remount,rw /`
   - Proceed with your secure operations

   **macOS:** - If you have an improvement suggestions, please go into [Pull Requests](https://github.com/neutronstar03/secrets-handbook/pulls)
   - Shut down your Mac
   - Power on your Mac and immediately press and hold the Shift key
   - Keep holding Shift until you see the login screen
   - Log in to your account (you might need to log in twice)
   - "Safe Boot" should appear in the top-right corner of the login screen

2. Verify you have no internet connection
3. Thoroughly check your browser extensions - remove any that could compromise security

### Step 2: Generate Seed Phrase

1. Open the `bip39-standalone.html` file in your browser
2. The tool will generate a seed phrase (choose 12 or 24 words)

   ![BIP39 Tool Interface](/images/bip39_01.png)

3. This seed should remain offline and will only be used to derive your wallet keys
4. Select "ETH - Ethereum" in the "Coin" dropdown (or your preferred cryptocurrency)
5. The "Derived Addresses" section will display your public/private key pairs

### Step 3: Secure Your Environment

1. Ensure your physical surroundings are private
2. Check that no one can view your screen
3. Consider using privacy screens or curtains

### Step 4: Import Private Keys to Wallets

1. In the "Derived Addresses" section, hover over a private key to display its QR code

   ![QR Code for Private Key](/images/bip39_02.png)

2. Scan this QR with your smartphone to import the specific address to your wallet
3. Label your wallets appropriately for future reference

### Step 5: Encrypt Your Seed Phrase

1. Open the `symmetro-v2.0.0.html` file in your browser
2. Copy your seed phrase into the "Encrypt" section
   - You can include additional notes or multiple seeds
   - The tool supports multiline text
3. Enter your memorized password in the "Password" field
4. Click "Encrypt"

   ![Symmetro Encryption Tool](/images/symmetro_01.png)

5. Save the encrypted text to a file
6. This encrypted file is secure enough to store in various locations

### Step 6: Verification and Completion

1. To verify, copy the encrypted text to the "Decrypt" section
2. Enter your password - you should see a checkmark ✅
3. Click "Decrypt" to view your original text (only do this in a secure environment)
4. Reboot your machine to normal mode
5. Your wallets are now ready to use with the imported keys

## Best Practices

- Never store your unencrypted seed phrase digitally
- Consider storing your encrypted backup in multiple secure locations
- Regularly verify that you can still decrypt your backup, in extreme case, you can still export your private keys and save them encrypted.
- Review this security process annually as tools and best practices evolve

## Security Warnings

- A malicious browser extension could potentially capture your clipboard data
- **Always** perform these steps offline in safe mode

---
