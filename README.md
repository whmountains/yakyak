# YakYak

[![Greenkeeper badge](https://badges.greenkeeper.io/yakyak/yakyak.svg)](https://greenkeeper.io/)

[![Build Status](https://travis-ci.org/yakyak/yakyak.svg)](https://travis-ci.org/yakyak/yakyak)

This is a fork of YakYak to fix a [bug](https://github.com/yakyak/yakyak/issues/918) where the app would get stuck on the loading screen. The maintainers appear to be unavailable so I made this as a temporary solution.

### Download Links

* [yakyak-1.5.1-linux-ia32.tar.gz](https://rawgit.com/whmountains/yakyak/master/dist/yakyak-1.5.1-linux-ia32.tar.gz)
* [yakyak-1.5.1-linux-x64.tar.gz](https://rawgit.com/whmountains/yakyak/master/dist/yakyak-1.5.1-linux-x64.tar.gz)
* [yakyak-1.5.1-osx.zip](https://rawgit.com/whmountains/yakyak/master/dist/yakyak-1.5.1-osx.zip)
* [yakyak-1.5.1-win32-ia32.tar.gz](https://rawgit.com/whmountains/yakyak/master/dist/yakyak-1.5.1-win32-ia32.zip)
* [yakyak-1.5.1-win32-x64.tar.gz](https://rawgit.com/whmountains/yakyak/master/dist/yakyak-1.5.1-win32-x64.zip)

---

Desktop client for Google Hangouts

![sshot](https://cloud.githubusercontent.com/assets/123929/16032313/cdba46c2-3204-11e6-912f-a72fef60563a.png)

(This app is in no way associated with or endorsed by Google)

## Install it

We provide [prebuilt binaries](https://github.com/yakyak/yakyak/releases) for macOS, Linux 32 / 64 and Windows 32 / 64. This is the [latest release](https://github.com/yakyak/yakyak/releases/latest)

Check out our wiki for [additional installation methods](https://github.com/yakyak/yakyak/wiki)

We love [bug reports](https://github.com/yakyak/yakyak/issues)!

## What does it do:

* Send/receive chat messages
* Create/change conversations (rename, add people)
* Leave/delete conversation
* Notifications (using native OS notifications)
  * Toggle notifications on/off
* Drag-drop, copy-paste or attach-button for image upload.
* Hangupsbot sync room aware (no bot name, proper user pics)
* Show inline images
* Send presence/focus/typing/activeclient to behave like a proper client
* History scrollback
* Video/audio integration (open in chrome)
* Focus/typing indications (mainly a design issue. keep it clean)
* Offer alternative color schemes
* Translations in 22 languages so far:
  * English / Portuguese _(Portugal and Brazil)_ / French / Spanish / Czech / German / Polish / Russian / Hebrew / Ukrainian / Slovenian / Korean / Tamil / Romanian / Swedish / Japanese / Italian / Danish / Bengali / Slovak / Turkish
  * We're looking for volunteers to translate the app to new languages

![sshot1](https://cloud.githubusercontent.com/assets/123929/16032393/991d63f8-3205-11e6-98bf-31f1b57cdc96.png)

![sshot2](https://cloud.githubusercontent.com/assets/123929/16032394/9e2ac08e-3205-11e6-81cc-fd4cb37441b5.png)

**NOTE**

Yakyak may show up as iOS Device and Google may alert you that _"some iOS Device is trying to use your account"_. This is normal as yakyak is an unofficial client and it mimics the behaviour of an iOS device in order to establish a communication with Google Hangout APIs.

## Credits

#### Main authors

* [Davide Bertola](https://github.com/davibe)
* [Martin Algesten](https://github.com/algesten)

#### Contributors

* [David Banham](https://github.com/davidbanham)
* [Max Kueng](https://github.com/maxkueng)
* [Arnaud Riu](https://github.com/arnriu)
* [Austin Guevara](https://github.com/austin-guevara)
* [André Veríssimo](https://github.com/averissimo)

## Developing

This is an open source project. Please help us!

It is written in coffeescript (nodejs) based on
[hangupsjs](https://github.com/algesten/hangupsjs) using
[trifl](http://algesten.github.io/trifl/) on top of
[electron (atom shell)](https://github.com/electron/electron).

### How can you help?

You can improve YakYak in many ways:

* Core functionality
* Interface _(example: new themes only require choosing less than 20 colors)_
* Bug fixing
* Translations _(new translation only need 117 strings)_

Send a pull request, start a conversation with a
[new issue](https://github.com/yakyak/yakyak/issues/new) or participate on a
[ongoing conversation](https://github.com/yakyak/yakyak/issues).

### Setup

Requirements:

* Node.js (v4 or v6)

```bash
$ npm install
$ npm run gulp
```

### Continuous build

```bash
$ npm run gulp watch
```

### Run it

```bash
$ npm run electron app
```

### Build Binaries for Deployment

_Supported platforms:_ Windows (_win32_), Mac OS X (_darwin_), Linux (_linux_)

_Suported architectures:_ 64-bits (_x64_), 32-bits (_ia32_)

```bash
# Building for all platforms and architectures
$ npm run deploy

# You can also build specific builds by using
#  deploy:<platform>-<architecture>
# example:
$ npm run deploy:darwin-x64
```

If you have [fpm](https://github.com/jordansissel/fpm) installed (`gem install fpm`), you can also build RPM and Deb packages:

```bash
$ npm run deploy:linux-x64:rpm
$ npm run deploy:linux-x64:deb
```

_note:_ if you are building _Windows_ binaries in _Linux_ or _Mac OS X_, Wine (1.6 or higher) must be installed. It also requires a 32-bit Wine installation when building Windows 32-bit binary.

### Structure

| Location  | Description                              |
| --------- | ---------------------------------------- |
| `src/`    | Is where sources live                    |
| `src/ui/` | Holds renderer code (client side)        |
| `dist/`   | Everything is compiled to this directory |

### Acknowledgement

* All the users and developers of YakYak
* ["You wouldn't believe"](https://notificationsounds.com/notification-sounds/you-wouldnt-believe-510) as the 'new message' sound for some platforms and is licensed under CC
