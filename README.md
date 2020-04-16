# PyInstaller Extractor

PyInstaller Extractor is a Python script to extract the contents of a PyInstaller generated Windows executable file.

<p align="center"><b>This is the snap for <a href="https://github.com/extremecoders-re/pyinstxtractor">PyInstaller Extractor</a>.</b> It works on Ubuntu, Fedora, Debian, and other major Linux
distributions.</p>


<p align="center">Published for <img src="http://anything.codes/slack-emoji-for-techies/emoji/tux.png" align="top" width="24" /> with :gift_heart: by Khiem Doan</p>

Source: [https://github.com/extremecoders-re/pyinstxtractor](https://github.com/extremecoders-re/pyinstxtractor)

PyInstaller Extractor is a Python script to extract the contents of a PyInstaller generated Windows executable file. The contents of the pyz file (usually pyc files) present inside the executable are also extracted.

The header of the pyc files are automatically fixed so that a Python bytecode decompiler will recognize it. The script can run on both Python 2.x and 3.x. Pyinstaller versions 2.0, 2.1, 3.0, 3.1, 3.2, 3.3, 3.4, 3.5 and 3.6 are tested & supported. Probably will work with other versions too.

This project was originally hosted on [SourceForge](https://sourceforge.net/projects/pyinstallerextractor/).

## How to install

```
sudo snap install pyinstxtractor
```

## How to use

The script can be run by passing the name of the exe as an argument.

```
$ pyinstxtractor <filename>
```

It is recommended to run the script in the same version of Python which was used to generate the executable. This is to prevent unmarshalling errors(if any) while extracting the PYZ archive.

## Example

```
$ pyinstxtractor test.exe
[+] Processing dist\test.exe
[+] Pyinstaller version: 2.1+
[+] Python version: 36
[+] Length of package: 5612452 bytes
[+] Found 59 files in CArchive
[+] Beginning extraction...please standby
[+] Possible entry point: pyiboot01_bootstrap.pyc
[+] Possible entry point: test.pyc
[+] Found 133 files in PYZ archive
[+] Successfully extracted pyinstaller archive: dist\test.exe

You can now use a python decompiler on the pyc files within the extracted directory
```

After extracting the pyc's you can use a Python decompiler like [Uncompyle6](https://github.com/rocky/python-uncompyle6/) or [pycdc](https://snapcraft.io/pycdc).

## Extracting Linux ELF binaries

Pyinstxtractor can also extract Linux ELF binaries. Please see the [Wiki](https://github.com/extremecoders-re/pyinstxtractor/wiki/Extracting-Linux-ELF-binaries) for more information.

For other questions, please see the [FAQ](https://github.com/extremecoders-re/pyinstxtractor/wiki/Frequently-Asked-Questions)
