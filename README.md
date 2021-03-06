# g-chat-electron
[![Build Status](https://travis-ci.org/Jiri-Kremser/g-chat-electron.svg?branch=master)](https://travis-ci.org/Jiri-Kremser/g-chat-electron)
[![npm version](https://badge.fury.io/js/g-chat-electron.svg)](https://badge.fury.io/js/g-chat-electron)



Simple [Electron](http://electron.atom.io) application that works as a desktop client
for chat.google.com.


## Usage

The simplest way to install the app is installing from npmjs.com:

```bash
sudo npm i -g electron --unsafe-perm=true
sudo npm i -g g-chat-electron
gChat
```

For dark theme, run the app with

```bash
gChat -d
```

## Getting started

- Install [Node LTS](https://nodejs.org)
- Clone this repository
- `npm install` to install the application's dependencies
- `npm start`

### Binary and rpm

#### Prerequisities
If you want to generate RPM package, it requires the `rpm-build` package to be installed

```
sudo dnf install rpm-build lsb
```

### Generate binaries

```
npm run binaries
ls dist/gChat-*
```

### Generate RPM

```
npm run binaries
npm run rpm
ls ./dist/installers/
```

### Gnome Desktop Entry

Provided you've installed the app via `npm i -g ..`, you can add the desktop entry by:

```bash
cat << EOF > ~/.local/share/applications/google-chat.desktop
[Desktop Entry]
Type=Application
Encoding=UTF-8
Name=Google Chat
Comment=Google Chat Destop App
Exec=/usr/bin/gChat -d
Icon=/usr/lib/node_modules/g-chat-electron/assets/icon.png
Terminal=false
EOF
```
