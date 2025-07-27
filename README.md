# GRIP.X - Jarvis AI Assistant

🤖 **GRIP.X** is an AI assistant project featuring a smart launcher called **Jarvis** that automatically manages your Python environment and dependencies.

## 🚀 Quick Start

### Running Jarvis

Simply run the launcher script:

```bash
./jarvis
```

Or with bash explicitly:

```bash
/bin/bash jarvis
```

### Manual Virtual Environment Activation

If you prefer to activate the virtual environment manually:

```bash
source .venv/bin/activate
```

## ✨ Features

- **🔧 Auto Environment Setup**: Automatically creates and activates Python virtual environment
- **📦 Dependency Management**: Installs and updates required packages automatically  
- **🐍 Python Compatibility**: Uses `python3` explicitly to avoid compatibility issues
- **📝 Smart Project Structure**: Auto-generates basic project files if missing
- **🎯 Cross-Platform**: Works on Linux, macOS, and Windows (with WSL/Git Bash)

## 🛠️ What the Script Does

1. **Checks for virtual environment** - Creates one if missing
2. **Activates the environment** - Ensures clean Python environment
3. **Upgrades pip** - Uses latest package installer
4. **Installs dependencies** - From requirements.txt (creates basic one if missing)
5. **Runs your application** - Looks for main.py, jarvis.py, or app.py

## 🔧 Troubleshooting

### "python: command not found" Error

This was the original issue you encountered. The script now:
- Uses `python3` explicitly instead of `python`
- Creates a symlink from `python` to `python3` in the virtual environment
- Handles missing virtual environment gracefully

### Missing Dependencies

The script automatically creates a `requirements.txt` with basic packages:
- `requests` - HTTP library
- `python-dotenv` - Environment variable management  
- `colorama` - Cross-platform colored terminal text

## 📂 Project Structure

```
GRIP.X/
├── jarvis              # Main launcher script
├── .venv/             # Virtual environment (auto-created)
├── requirements.txt   # Python dependencies (auto-created)
├── main.py           # Main application (auto-created)
└── README.md         # This file
```

## 🎯 Next Steps

Extend your Jarvis assistant by adding:
- Speech recognition capabilities
- Integration with AI APIs (OpenAI, etc.)
- Voice synthesis
- Task automation features
- Custom commands and workflows

## 💡 Development

After running `./jarvis` once, you can develop with the activated environment:

```bash
source .venv/bin/activate
python main.py  # or any other Python script
```

---

**Happy coding with Jarvis! 🤖✨**
