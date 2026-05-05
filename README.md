# machinetool plugin for MADS

This is a Sink plugin for [MADS](https://github.com/MADS-NET/MADS). 

This plugin visualizes on [Rerun](https://rerun.io) a 3D model of a machine tool, updating axes positions according to the received commands. It is just a viewer and does not provide any dinamics simulation. Foor that, head to <https://gitbub.com/mads-net/FMU_agent>.

*Required MADS version: 2.0.0.*


## Supported platforms

Currently, the supported platforms are:

* **Linux** 
* **MacOS**
* **Windows**


## Build from source

Linux and MacOS:

```bash
cmake -Bbuild -DCMAKE_INSTALL_PREFIX="$(mads -p)"
cmake --build build -j4
sudo cmake --install build
```

Windows:

```powershell
cmake -Bbuild -DCMAKE_INSTALL_PREFIX="$(mads -p)"
cmake --build build --config Release
cmake --install build --config Release
```

## Install from release

Download a release from GitHub, unzip it, then:

## Requirement: Rerun

The easiest way to install the Rerun viewer is via pip:

```sh
python3 -mvenv .venv
source .venv/bin/activate # or, on Windows: .venv\script\activate.bat
pip install rerun-sdk==0.27.3
```

Then launch the agent from same shell.


## INI settings

The plugin supports the following settings in the INI file:

```ini
[machinetool]
# Describe the settings available to the plugin
```

All settings are optional; if omitted, the default values are used.




## Executable demo

<Explain what happens if the test executable is run>

---