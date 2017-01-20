# Windows-Build-Tools for Atom

[![Greenkeeper badge](https://badges.greenkeeper.io/lgeiger/windows-build-tools.svg)](https://greenkeeper.io/)

On Windows? Want to install [Atom](https://atom.io/) packages depending on native Node modules?

Install the build tools from an elevated PowerShell (run as Administrator) by running:
```powershell
apm install windows-build-tools --verbose
apm config set msvs_version 2015
apm config set python $env:USERPROFILE\.windows-build-tools\python27\python.exe
```

It will install [Windows Build Tools](https://github.com/felixrieseberg/windows-build-tools) by Felix Rieseberg without needing a separate [Node.js](https://nodejs.org/) installation:

> After installation, npm will automatically execute this module, which downloads and installs Visual C++ Build Tools 2015, provided free of charge by Microsoft. These tools are required to compile popular native modules. It will also install Python 2.7, configuring your machine and npm appropriately.

> > :bulb: [Windows Vista / 7 only] requires .NET Framework 4.5.1 (Currently not installed automatically by this package)

> Both installations are conflict-free, meaning that they do not mess with existing installations of Visual Studio, C++ Build Tools, or Python. If you see anything that indiciates otherwise, please file a bug.

To verify that everything worked run:
```powershell
apm install --check
```
