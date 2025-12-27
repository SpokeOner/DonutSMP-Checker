# DonutSMP Checker

> **⚠️ DISCLAIMER: This project is for EDUCATIONAL and LEARNING PURPOSES ONLY.**
> 
> This software is provided for educational purposes to help developers understand authentication flows, API integration, and web scraping techniques. The use of this software to check accounts without explicit authorization is strictly prohibited and may violate terms of service and applicable laws. The authors and contributors are not responsible for any misuse of this software.

A Minecraft account checker for DonutSMP with support for various account types, stats checking, and Discord webhooks.

## Features

- ✅ DonutSMP stats checking (money, kills, deaths, playtime, etc.)
- ✅ Account type detection (Normal Minecraft, Xbox Game Pass, etc.)
- ✅ Email access checking
- ✅ Optifine cape detection
- ✅ Name change availability checking
- ✅ Payment information extraction
- ✅ Discord webhook notifications
- ✅ Proxy support (HTTP, SOCKS4, SOCKS5)
- ✅ Auto proxy scraper
- ✅ Multi-threaded checking

## Setup

1. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
   
   Or manually:
   ```bash
   pip install requests colorama readchar configparser urllib3
   ```
   
   **Note:** If you get an error about `console.utils`, you may need to install it separately or remove that import if you don't need the title setting feature.

2. **Configure `config.ini`:**
   - The `config.ini` file is already in the repo with placeholders
   - Add your Discord webhook URLs
   - Add your DonutSMP API key
   - (Optional) Add email check API URL if you have one
   - Configure capture options and auto actions

3. **Prepare your files:**
   - Create a combo file with `email:password` format (one per line)
   - (Optional) Create a proxy file with proxies in `ip:port` or `user:pass@ip:port` format

4. **Run the checker:**
   ```bash
   python MSMC.py
   ```

## Configuration

### Required Settings

- **Webhook**: Main Discord webhook for hits
- **DonutSMP API Key**: Your DonutSMP API key

### Optional Webhooks

- **Hits Webhook**: Separate webhook for all hits
- **2FA Webhook**: Webhook for 2FA accounts
- **Xbox Webhook**: Webhook for Xbox Game Pass accounts
- **Other Webhook**: Webhook for other account types

### Proxy Types

1. HTTP/HTTPS
2. SOCKS4
3. SOCKS5
4. None (proxyless)
5. Auto Scraper (scrapes free proxies)

## Usage

1. Run `MSMC.py`
2. Enter number of threads (recommended: 100 with proxies, max 5 proxyless)
3. Select proxy type
4. Choose screen mode (CUI or Log)
5. Select your combo file
6. (If not using auto scraper) Select your proxy file
7. Wait for results in `results/` folder

## Results

Results are saved in `results/[filename]/`:
- `Hits.txt` - All valid accounts
- `Capture.txt` - Full capture details
- `2fa.txt` - 2FA accounts
- `XboxGamePass.txt` - Xbox Game Pass accounts
- `XboxGamePassUltimate.txt` - Xbox Game Pass Ultimate accounts
- `Normal.txt` - Normal Minecraft accounts
- `Other.txt` - Other account types
- `Valid_Mail.txt` - Valid email accounts
- `MFA.txt` - Full email access accounts
- `SFA.txt` - No email access accounts
- `Payment.txt` - Payment information
- `Codes.txt` - Xbox buddy pass codes

## Notes

- Make sure you have a valid DonutSMP API key
- Email check API is optional - if not provided, email access checking will be skipped
- Use proxies to avoid rate limits
- Results are automatically saved and sent to Discord webhooks

## ⚠️ Legal Disclaimer

**THIS SOFTWARE IS PROVIDED FOR EDUCATIONAL AND LEARNING PURPOSES ONLY.**

- This project is intended solely for educational purposes to demonstrate programming concepts, API integration, and authentication mechanisms.
- **DO NOT** use this software to check accounts without explicit authorization from the account owner.
- Unauthorized access to accounts is illegal and violates terms of service.
- The authors, contributors, and maintainers of this project are **NOT RESPONSIBLE** for any misuse, damage, or legal consequences resulting from the use of this software.
- Users are solely responsible for ensuring their use of this software complies with all applicable laws and terms of service.
- By using this software, you agree to use it responsibly and legally.

**Use at your own risk. Educational purposes only.**

## License

This project is provided for educational and learning purposes only. See the disclaimer above.

