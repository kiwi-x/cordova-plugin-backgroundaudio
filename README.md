Attention - we just removed the modification of the info plist file to! - No other changes


# BackgroundAudio - a Cordova plugin
by [Eddy Verbruggen](http://twitter.com/eddyverbruggen)

## 0. Index

1. [Description](#1-description)
2. [Installation](#2-installation)
3. [Usage](#3-usage)
4. [License](#4-license)

## 1. Description

Allows your app to keep on playing audio when it's in the background.

* Compatible with [Cordova Plugman](https://github.com/apache/cordova-plugman).
* For iOS only.

## 2. Installation

### Automatically (CLI / Plugman)
Compatible with [Cordova Plugman](https://github.com/apache/cordova-plugman), compatible with [PhoneGap 3.0 CLI](http://docs.phonegap.com/en/3.0.0/guide_cli_index.md.html#The%20Command-line%20Interface_add_features), here's how you fetch the latest release from npm with the Cordova CLI:

```
$ cordova plugin add nl.x-services.plugins.backgroundaudio
```

or, the latest from GitHub:
```
$ cordova plugin add https://github.com/EddyVerbruggen/cordova-plugin-backgroundaudio
```

### Manually

1\. Add the following xml to your `config.xml` in the root directory of your `www` folder:
```xml
<feature name="BackgroundAudio">
  <param name="ios-package" value="BackgroundAudio" />
  <param name="onload" value="true" />
</feature>
```

2\. Download the source files and copy them to your project.

iOS: Copy the `.h` and `.m` files to `platforms/ios/<ProjectName>/Plugins`

3\. Open your `<ProjectName>-Info.plist` and add a key `UIBackgroundModes` with an array value `audio`.

## 3. Usage
Nothing to do here as the plugin will call the required native code on load automatically :)

### 3.1 Another Use-Case
When developing a app with media in it, the volume of the ringtone defines the volume of the media. So when the ringtone is muted, the sound of the media is muted. With this plugin installed, the volume of the media in the app is defined by the media volume of the phone.

Having only this Use-Case, your app may get rejected in the App Store, because you are not using the background feature. You have to remove the `audio` array in the `UIBackgroundModes` section manually in the `<ProjectName>-Info.plist` file

## 4. License

[The MIT License (MIT)](http://www.opensource.org/licenses/mit-license.html)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
