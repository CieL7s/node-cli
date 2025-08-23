# JavaScript CLI Wrapper (jcli)

<div align="center">

![CLI Banner](https://img.shields.io/badge/CLI-Wrapper-brightgreen.svg)
![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Node](https://img.shields.io/badge/node-%3E%3D12.0.0-green.svg)
![License](https://img.shields.io/badge/license-MIT-yellow.svg)

**A Pterodactyl-inspired CLI wrapper for running system commands with style** 🚀

*Built by CieLV7*

</div>

---

## 📋 Table of Contents

- [Features](#-features)
- [Installation](#-installation)
- [Quick Start](#-quick-start)
- [Configuration](#-configuration)
- [Commands](#-commands)
- [Usage Examples](#-usage-examples)
- [Development](#-development)
- [Contributing](#-contributing)
- [License](#-license)

---

## ✨ Features

- 🎯 **Pterodactyl-inspired interface** - Clean, professional command-line experience
- 🔧 **100+ Built-in commands** - Comprehensive set of system utilities
- 🚀 **Process management** - PM2 integration for application lifecycle
- 🐳 **Docker support** - Container management commands
- 📦 **Package management** - NPM, pip, apt, yum support
- 🌐 **Git integration** - Version control commands
- 📊 **System monitoring** - Resource usage and system information
- 📁 **File operations** - Complete file system management
- 🔄 **Command aliases** - Shortcuts for frequently used commands
- 📜 **Command history** - Track and replay previous commands
- ⚡ **Performance optimized** - Fast command execution with proper error handling

---


## 🏁 Quick Start

1. **Start the CLI**:
   ```bash
   jcli
   ```

2. **Run your first command**:
   ```bash
   [WhatsApp] project $ help
   ```

3. **Execute system commands**:
   ```bash
   [WhatsApp] project $ terminal ls -la
   # or simply
   [WhatsApp] project $ ls
   ```

4. **Get system information**:
   ```bash
   [WhatsApp] project $ neofetch
   ```

---

## ⚙️ Configuration

The CLI uses `ptero-config.json` for configuration. If not found, it creates default settings.

### Default Configuration

```json
{
    "name": "WhatsApp Bot Environment",
    "shell": "/bin/bash",
    "workingDir": "/current/directory",
    "nodeVersion": "v18.x.x",
    "env": {
        "NODE_ENV": "production",
        "PTERO_SERVER": "true"
    },
    "startupCommand": "npm start",
    "allowedCommands": ["all"]
}
```

### Extended Configuration (cli-config.json)

```json
{
    "environment": {
        "NODE_ENV": "production",
        "PTERO_SERVER": "true",
        "SERVER_MEMORY": "1024",
        "SERVER_IP": "0.0.0.0",
        "SERVER_PORT": "3000"
    },
    "pteroCommands": {
        "start-bot": {
            "description": "Start WhatsApp bot",
            "command": "npm start"
        }
    },
    "aliases": {
        "start": "start-bot",
        "sys": "neofetch"
    }
}
```

---

## 📚 Commands

### 🔧 Core Commands

| Command | Description | Example |
|---------|-------------|---------|
| `terminal <cmd>` | Execute any terminal command | `terminal ls -la` |
| `run <cmd>` | Alias for terminal | `run node --version` |
| `exec <cmd>` | Another terminal alias | `exec git status` |
| `kill` | Kill current running process | `kill` |
| `restart` | Restart application | `restart` |
| `status` | Show server status | `status` |

### 📊 System Information

| Command | Description | Output |
|---------|-------------|---------|
| `neofetch` | Display system info | OS, CPU, Memory, etc. |
| `sysinfo` | Alternative system info | Same as neofetch |
| `info` | Server information | Config and runtime info |

### ⚙️ Process Management (PM2)

| Command | Description | Usage |
|---------|-------------|-------|
| `pm2-start` | Start PM2 process | `pm2-start app.js` |
| `pm2-stop` | Stop PM2 process | `pm2-stop app` |
| `pm2-restart` | Restart PM2 process | `pm2-restart all` |
| `pm2-list` | List PM2 processes | `pm2-list` |
| `pm2-logs` | Show PM2 logs | `pm2-logs app` |

### 📦 Node.js & NPM

| Command | Description | Usage |
|---------|-------------|-------|
| `node-version` | Show Node.js version | `node-version` |
| `npm-install` | Install NPM packages | `npm-install express` |
| `npm-start` | Start NPM application | `npm-start` |
| `npm-run` | Run NPM script | `npm-run dev` |
| `npm-list` | List installed packages | `npm-list` |

### 🐍 Python Support

| Command | Description | Usage |
|---------|-------------|-------|
| `python` | Run Python command | `python script.py` |
| `python3` | Run Python3 command | `python3 --version` |
| `pip` | Python package installer | `pip install requests` |
| `pip3` | Python3 package installer | `pip3 list` |

### 📁 File Operations

| Command | Description | Usage |
|---------|-------------|-------|
| `ls` | List directory contents | `ls /home` |
| `cd` | Change directory | `cd /var/www` |
| `pwd` | Print working directory | `pwd` |
| `cat` | Display file contents | `cat config.json` |
| `mkdir` | Create directory | `mkdir new-folder` |
| `rm` | Remove files/directories | `rm -rf old-folder` |
| `cp` | Copy files | `cp file.txt backup.txt` |
| `mv` | Move/rename files | `mv old.txt new.txt` |

### 🔀 Git Commands

| Command | Description | Usage |
|---------|-------------|-------|
| `git` | Git commands | `git commit -m "message"` |
| `git-clone` | Clone repository | `git-clone repo-url` |
| `git-pull` | Pull from repository | `git-pull` |
| `git-push` | Push to repository | `git-push` |
| `git-status` | Git status | `git-status` |
| `git-log` | Git log (last 10) | `git-log` |

### 🐳 Docker Commands

| Command | Description | Usage |
|---------|-------------|-------|
| `docker` | Docker commands | `docker run nginx` |
| `docker-ps` | List containers | `docker-ps` |
| `docker-images` | List images | `docker-images` |
| `docker-build` | Build image | `docker-build -t myapp .` |

### 🌐 Network & Monitoring

| Command | Description | Usage |
|---------|-------------|-------|
| `ping` | Ping host | `ping google.com` |
| `curl` | HTTP requests | `curl https://api.github.com` |
| `wget` | Download files | `wget file-url` |
| `ps` | Process list | `ps` |
| `top` | System monitor | `top` |
| `htop` | Interactive monitor | `htop` |
| `df` | Disk usage | `df` |
| `free` | Memory usage | `free` |
| `uptime` | System uptime | `uptime` |

### 🛠️ CLI Management

| Command | Alias | Description |
|---------|-------|-------------|
| `help` | `h`, `?` | Show help menu |
| `commands` | - | List all commands |
| `history` | - | Show command history |
| `clear` | `c`, `cls` | Clear screen |
| `exit` | `q`, `x` | Exit CLI |

---

## 💡 Usage Examples

### Basic System Management

```bash
# Check system information
[WhatsApp] project $ neofetch

# Monitor system resources
[WhatsApp] project $ free
[WhatsApp] project $ df

# Check running processes
[WhatsApp] project $ ps
```

### Application Development

```bash
# Install dependencies
[WhatsApp] project $ npm-install

# Start development server
[WhatsApp] project $ npm-run dev

# Monitor with PM2
[WhatsApp] project $ pm2-start app.js --name "myapp"
[WhatsApp] project $ pm2-logs myapp
```

### File Operations

```bash
# Navigate and explore
[WhatsApp] project $ ls
[WhatsApp] project $ cd src
[WhatsApp] src $ pwd

# File management
[WhatsApp] src $ cat package.json
[WhatsApp] src $ cp config.example.json config.json
```

### Git Workflow

```bash
# Check repository status
[WhatsApp] project $ git-status

# Pull latest changes
[WhatsApp] project $ git-pull

# View recent commits
[WhatsApp] project $ git-log
```

### Docker Operations

```bash
# List containers
[WhatsApp] project $ docker-ps

# Build and run
[WhatsApp] project $ docker-build -t myapp .
[WhatsApp] project $ terminal docker run -p 3000:3000 myapp
```

---

## 🛠️ Development

### Project Structure

```
js-cli-wrapper/
├── cli.js                 # Main CLI application
├── cli-config.json       # Extended configuration
├── ptero-config.json     # Runtime configuration
├── package.json          # NPM package configuration
├── README.md             # This file
└── test.js              # Test suite (optional)
```


### Adding Custom Commands

You can extend the CLI by modifying the `setupPteroCommands()` method in `cli.js`:

```javascript
// Add your custom command
this.addCommand('my-command', 'My custom command', (args) => {
    console.log('Hello from my custom command!');
    // Your command logic here
});

// Add alias
this.aliases.set('mc', 'my-command');
```

---

## 🤝 Contributing

We welcome contributions! Please follow these guidelines:

1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/amazing-feature`
3. **Commit** your changes: `git commit -m 'Add amazing feature'`
4. **Push** to the branch: `git push origin feature/amazing-feature`
5. **Open** a Pull Request

### Development Guidelines

- Follow existing code style
- Add tests for new features
- Update documentation
- Ensure backward compatibility

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Inspired by Pterodactyl Panel's command interface
- Built with ❤️ for the developer community
- Special thanks to all contributors

---

## 📞 Support

- 📧 **Issues**: [GitHub Issues](https://github.com/yourusername/js-cli-wrapper/issues)
- 💬 **Discussions**: [GitHub Discussions](https://github.com/yourusername/js-cli-wrapper/discussions)
- 📖 **Wiki**: [Project Wiki](https://github.com/yourusername/js-cli-wrapper/wiki)

---

<div align="center">

**Made with ❤️ by CieLV7**

![Footer](https://img.shields.io/badge/⭐-Star%20this%20repo-yellow.svg)

</div>
