# 16-bit EXE Runner

Run classic **16-bit DOS programs and games directly in your web browser** using [js-dos](https://js-dos.com/) and DOSBox.

## ✨ Features

* 🖥️ Run DOS `.EXE` and `.COM` programs in your browser
* 🎮 Run classic DOS games
* 📦 Load additional files required by programs
* 💾 Virtual DOS filesystem
* ⏯️ Pause and resume emulation
* 🔄 Restart programs
* ⛶ Fullscreen mode
* 📋 Copy and clear debug logs
* 🔍 Inspect executable file headers
* 📊 Display program format and file information
* 🌐 Runs entirely in the browser

## 🚀 Supported Programs

The runner is designed primarily for:

* **16-bit DOS EXE files**
* **DOS COM programs**
* **DOS batch files (`.BAT` / `.CMD`)**
* Classic DOS games
* Older DOS utilities and applications

### ⚠️ Windows EXE Compatibility

Not every `.EXE` file is a DOS executable.

Modern Windows programs usually use the **PE (Portable Executable)** format and cannot be run directly by this project.

Some older Windows programs use the **NE (New Executable)** format and require a compatible Windows 3.x/Windows 9x environment rather than plain DOSBox.

The runner checks the executable header and reports the detected format.

## 🛠️ How It Works

The project uses **js-dos v8**, which provides a browser-based DOSBox environment powered by WebAssembly.

When you select a program:

1. The executable is inspected.
2. Selected files are placed into a virtual DOS filesystem.
3. DOSBox is started in the browser.
4. The program is launched through DOS.
5. Output is displayed in the emulator screen.

No native Windows installation is required.

## 🌐 Running the Project

Because js-dos uses WebAssembly and browser resources, the project should be served over **HTTP/HTTPS**.

For example, you can host it with:

* GitHub Pages
* A local web server
* Any static web hosting service

Opening the HTML directly with `file://` may prevent the emulator from loading correctly.

## 📁 Example

You can select:

```text
GAME.EXE
```

or, if the program needs additional files:

```text
GAME.EXE
DATA.DAT
CONFIG.CFG
SOUND.DAT
```

The selected files are placed into the virtual DOS `C:` drive before the program starts.

## 📋 Requirements

* A modern web browser
* JavaScript enabled
* WebAssembly support
* HTTP/HTTPS hosting

## 🔧 Technology

* HTML
* CSS
* JavaScript
* [js-dos](https://js-dos.com/)
* DOSBox
* WebAssembly
