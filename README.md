# PassForge 🔐 [![GitHub License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

**Advanced password list generator with hybrid mutation engine and wordlist integration**

![PassForge Demo](logo_password.png)

## Features ✨
- **15+ Generation Patterns** (Leet, Padding, Year Suffix) :cite[1]
- **Wordlist Integration** (RockYou, Xato, Custom) :cite[5]
- **Glassmorphism UI** with real-time preview
- **Standalone EXE** build support
- **Ngrok Tunnel** integration for remote access

## requirements.txt (Dependencies)

flask==3.0.2
pyinstaller==6.0.0
waitress==3.0.0
python-dotenv==1.0.0

## Installation 🛠️
```bash
# Clone repo
git clone https://github.com/yourusername/PassForge
cd PassForge

# Install dependencies
pip install -r setup/requirements.txt
```

## Usage 🚀 
```bash
# Local execution
python -m waitress --port=5000 app:app

# Remote access via Ngrok
ngrok_config/ngrok.bat
```
**Build ngrok.bat** *(Ngrok Tunnel)*
```bash
@echo off
start ngrok http 5000
python -m waitress --port=5000 app:app
```
## Wordlist Sources 📚

**Name	Entries	Use Case**
+ RockYou	32M	Common passwords [[download] - (https://github.com/kkrypt0nn/wordlists/blob/main/Passwords/rockyou.txt)](https://github.com/kkrypt0nn/wordlists/blob/main/Passwords/rockyou.txt)
+ Xato.Net 5.1M	Modern breaches [download - (https://github.com/kkrypt0nn/wordlists/blob/main/Passwords/xato-net-passwords.txt)]
+ Psudohash 7,776	Pattern-based mutations	[download - (https://github.com/t3l3machus/psudohash)]
+ CUPP custom	User-specific profiling	[download - (https://github.com/Mebus/cupp)]
+ EFF custom Wordlists	Passphrase generation	[download - (https://www.eff.org/deeplinks/2016/07/new-wordlists-random-passphrases)]

## Build executable
- **build_exe.bat** *(Windows Executable Builder)*
- *setup/build_exe.bat*
```bash
@echo off
pyinstaller --onefile --add-data "app;app" --add-data "wordlists;wordlists" --name PassForge app/routes.py
```

**Security Notice: Use only for authorized penetration testing. Never engage in illegal activities.**

##**Implementation Notes**
1. **Standalone EXE**: Uses PyInstaller with resource embedding
2. **Ngrok Integration**: Auto-starts tunnel with bat file:cite[3]
3. **Wordlist Management**: Pre-loaded + dynamic download system
4. **Security**: Rate limiting & input sanitization

