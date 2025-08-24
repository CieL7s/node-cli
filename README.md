# JAVASCRIPT CLI WRAPPER (JCLI)

![Version](https://img.shields.io/badge/version-2.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Node](https://img.shields.io/badge/node-%3E%3D14.0.0-brightgreen.svg)

An advanced, stylized terminal interface built with Node.js featuring colorful ASCII art, system monitoring, and command execution capabilities.

## 🚀 Features

- **Beautiful ASCII Art Interface** - Eye-catching terminal design with colored output
- **System Information Display** - Real-time system stats including CPU, memory, uptime, and network interfaces
- **Command Execution** - Execute any system command directly through the interface
- **Interactive Help System** - Built-in help commands and documentation
- **Graceful Error Handling** - Proper error messages and exit handling
- **Cross-platform Support** - Works on Windows, macOS, and Linux

## 📋 Prerequisites

- Node.js >= 14.0.0
- Terminal with ANSI color support

## 🛠 Installation

1. Clone or download the repository (private access required)
2. Navigate to the project directory
3. Install dependencies:
   ```bash
   npm install
   ```
4. For development:
   ```bash
   npm run dev
   ```
5. For production (obfuscated):
   ```bash
   npm run build
   node dist/cli.js
   ```

## 🎮 Usage

### Available Commands

| Command | Alias | Description |
|---------|-------|-------------|
| `help` | `?` | Show available commands |
| `clear` | `cls` | Clear the terminal screen |
| `sysinfo` | - | Display detailed system information |
| `exit` | `quit` | Exit the terminal interface |
| `[any command]` | - | Execute any system command |

### Examples

```bash
# Show system information
sysinfo

# Clear screen
clear

# Execute system commands
ls -la
ping google.com
ps aux

# Get help
help
```

## 🖥 Screenshots

When you run CieLV7, you'll see:

- Colorful ASCII art header with the CieLV7 logo
- System overview with hostname, platform, memory usage, CPU cores, etc.
- Interactive command prompt with timestamp
- Beautifully formatted output for all operations

## 🏗 Development & Build

### Development Mode
```bash
npm run dev
```

### Production Build (Obfuscated)
```bash
npm run build
```
This will create an obfuscated version in the `dist/` directory.

## 🏗 System Information Displayed

- **Hostname** - Current system hostname
- **Platform** - Operating system and architecture
- **Kernel** - OS kernel version
- **Uptime** - System uptime in hours and minutes
- **Memory Usage** - Used/Total/Free memory in GB
- **CPU Information** - Number of cores and detailed specs
- **Node.js Version** - Runtime version
- **Current User** - Active username
- **Network Interfaces** - IP addresses for network adapters
- **Load Average** - System load metrics

## 🎨 Customization

The interface uses ANSI color codes for styling. You can modify the colors by editing the `colors` object in the main file:

```javascript
const colors = {
  reset: '\x1b[0m',
  bright: '\x1b[1m',
  red: '\x1b[31m',
  green: '\x1b[32m',
  yellow: '\x1b[33m',
  blue: '\x1b[34m',
  cyan: '\x1b[36m',
  // ... add more colors
};
```

## 🔧 Technical Details

- **Built with**: Node.js core modules (os, readline, child_process)
- **No external dependencies** - Uses only Node.js built-in modules
- **Cross-platform** - Works on all major operating systems
- **Memory efficient** - Lightweight implementation
- **Real-time data** - Live system information updates

## 📝 File Structure

```
cielv7-terminal/
├── cli.js           # Main application file
├── package.json     # Package configuration
├── README.md        # This file
└── dist/            # Obfuscated production files
    └── cli.js       # Obfuscated main file
```

## 🤝 Contributing

This is a closed-source project. Contributing is by invitation only.

For bug reports or feature requests, please contact the maintainer directly.

## 📄 License

This project is proprietary and closed source. All rights reserved.

**⚠️ Important Notice:**
- This software is not open source
- Redistribution is not permitted
- Code is obfuscated for production use
- Contact the author for licensing inquiries

## 🐛 Known Issues

- Some terminal emulators may not fully support all ANSI color codes
- Command execution inherits the parent process environment

## 🔮 Future Enhancements

- [ ] Plugin system for custom commands
- [ ] Configuration file support
- [ ] Command history
- [ ] Auto-completion
- [ ] Themes support
- [ ] Performance monitoring graphs
- [ ] Log file generation

## 📧 Support

If you encounter any issues or have questions, please:

1. Check the existing issues on the repository
2. Create a new issue with detailed information
3. Include your OS, Node.js version, and terminal type

## 🎯 Version History

- **v2.0.0** - Current version with enhanced UI and system information
- **v1.0.0** - Initial release

---

**Made with ❤️ by CieLV7 Team**

*Enjoy your enhanced terminal experience!*
