[![Join the chat at https://gitter.im/zhuzhuyule/Lobby](https://badges.gitter.im/hexo-theme-tomotoes/Lobby.svg)](https://gitter.im/zhuzhuyule/Lobby?utm_source=share-link&utm_medium=link&utm_campaign=share-link) 
[![Document|ZH](https://camo.githubusercontent.com/f6977a970c4eaf235fb3b115069c08634611611c/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f646f63756d656e742d434e2d677265656e2e7376673f7374796c653d666c61742d737175617265)](doc/zh/README.md) 
[![License](https://img.shields.io/cocoapods/l/AFNetworking.svg)](https://zhuzhuyule.com)

# HexoEditor
This is markdown editor for Hexo.  

Built with Electron.

Inherit [Moeditor](https://github.com/Moeditor/Moeditor), I want to fix it appropriate to Hexo Blog !

Click here go to **[Download](https://github.com/zhuzhuyule/HexoEditor/releases)** page !

[中文.doc](doc/zh/README.md)
# QQ Group:
- Name：HexoEditor        
- QQID：602883087   
- PASS：HexoEditor           
- Data：2017-12-29  

# Features
* HexoEditor 
  * Hexo Post Preview same as in Browser
  * Hexo Tag/Filter/Renderer support
  * Custom tag support
  * Use Hexo `_config.yml` support
    * highlight setting
    * theme tag support
  * --------- v1.1.8 (2017-12-29) ---------
  * Quick New Post in hexo source 
  * Quick Modify File Name (In Hexo Post Edit)  
  * Shortcut Support
  * Editor Line number Show/Hide
  * Auto Show/Hide Scroll
  * Scorll Together/None
* HexoEditor (Inherit [Moeditor](https://github.com/Moeditor/Moeditor))
  * GitHub Flavored Markdown
  * TeX math expressions
  * UML diagrams
  * Code highlight in editor
  * Read/Write/Preview mode
  * Custom font / line height / font size
  * Custom themes
  * Code highlight themes (powered by [highlight.js](https://highlightjs.org/))
  * Auto reload
  * Localization
  * Focus mode

# Screenshots

![Moeditor Main](screenshots/main.png)

![Moeditor Write Mode](screenshots/side-menu.png)

![Moeditor Write Mode](screenshots/settings.png)

![Moeditor About](screenshots/about.png)

# Gif Screenshots
![Moeditor tag](screenshots/gif-tag.gif)

![Moeditor Mode](screenshots/gif-mode.gif)

![Moeditor New Post](screenshots/gif-newpost.gif)

![Moeditor Hexo](screenshots/gif-hexo.gif)

# Plan To Do
- [ ] Add Toc
- [ ] Add Hexo Title Header setting
.....
- [ ] Deploy Post
- [ ] Add multi-editing in tabs

# Building
```bash
npm install
npm start
```

In China, you may want to replace npm with cnpm for a faster download speed.

```bash
npm install cnpm -g --registry=https://registry.npm.taobao.org
cnpm install
cnpm start
```
# Debugging
There's three ways to open the [Chromium Developer Tools](https://developer.chrome.com/devtools).

* Add `--debug` to the command line args:
```bash
npm start -- --debug
```

* Set `debug` to `true` in the config. The config file is stored in `~/.config/configstore/Moeditor.json` (for every system).

* `Ctrl` + `Shift` + `I` in Linux / Windows or `Command` + `Option` + `I` in OS X / macOS to toggle devtools for a window.


# Localization
Moeditor will auto detect your system language and use the localization.

You can set language manually in the Settings window.

Now the app supports English, Chinese, French, German, Spanish and *incomplete* Portuguese.

**Help us** if you can translate this app. Please follow the guide in `app/moe-l10n.js`.

# License
Moeditor itself is licensed under the **GPL v3** license.

Some node modules are licensed under other free software license.

The `Raleway` font is licensed under the OFL open font license.

# Credits
The domain `moeditor.org` is sponsored by [Showfom](https://ttt.tt/).

# Tips
1. modify codemirror file :

> ./node_modules/codemirror/lib/codemirror.js (line: `3104`)


> ./node_modules/codemirror/src/display/selection.js (line: `56`)

```js 
//var rightSide = Math.max(display.sizerWidth, displayWidth(cm) - display.sizer.offsetLeft) - padding.right;
var rightSide = display.lineDiv.offsetWidth - padding.right;
```
