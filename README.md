# PassForge 🔐 [![GitHub License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

Advanced password list generator with hybrid mutation engine and wordlist integration

![PassForge Demo](logo_password.png)

## Features ✨
- **15+ Generation Patterns** (Leet, Padding, Year Suffix) :cite[1]
- **Wordlist Integration** (RockYou, Xato, Custom) :cite[5]
- **Glassmorphism UI** with real-time preview
- **Standalone EXE** build support
- **Ngrok Tunnel** integration for remote access

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

## Wordlist Sources 📚

+ Name	Entries	Use Case [link_coming_soon]
+ RockYou	32M	Common passwords [link_coming_soon]
+ Xato Net	5.1M	Modern breaches [link_coming_soon]
+  EFF Long	7,776	Secure passphrases2 [link_coming_soon]
+ CUPP	Custom	Targeted profiling11 [link_coming_soon]

# Build executable
setup/build_exe.bat# PassForge
generate password lists easily.

**Security Notice: Use only for authorized penetration testing. Never engage in illegal activities.**

### **Implementation Notes**
1. **Standalone EXE**: Uses PyInstaller with resource embedding
2. **Ngrok Integration**: Auto-starts tunnel with bat file:cite[3]
3. **Wordlist Management**: Pre-loaded + dynamic download system
4. **Security**: Rate limiting & input sanitization

