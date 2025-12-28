# SimpleEQ
A JUCE-based EQ plugin.

## How to Build
1. Clone the repository.
2. Ensure you have the [JUCE Framework](https://juce.com/download/) installed.
3. Open `SimpleEQ.jucer` in the Projucer (at `JUCE/extras/Projucer/Builds`)
4. Set your Global Paths to point to your JUCE folder if necessary.
5. Select the appropriate Exporter (e.g., Linux Makefile) and hit **Save**.
6. Navigate to `Builds/LinuxMakefile` and run `make`.
7. Your stand alone executable will be avaiable at `Builds/LinuxMakefile/build/SimpleEQ`

# Fix VSCode Showing Errors

If your vscode is showing red squigly lines in the include statements, create the file `.vscode/c_cpp_properties.json` and set the contents to:
```
{
    "configurations": [
        {
            "name": "Linux",
            "includePath": [
                "${workspaceFolder}/**",
                "/home/YOUR_USERNAME/JUCE/modules/**"
            ],
            "defines": [],
            "compilerPath": "/usr/bin/gcc",
            "cStandard": "c17",
            "cppStandard": "gnu++17",
            "intelliSenseMode": "linux-gcc-x64"
        }
    ],
    "version": 4
}
```
Or alternatively, press `Ctrl+Shift+P` and type C/C++: Edit Configurations (UI) and then add `/home/YOUR_USERNAME/JUCE/modules/**` to include path.

Make sure to replace YOUR_USERNAME by your actual username on the machine.