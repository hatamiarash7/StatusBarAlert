
[![Android Arsenal]( https://img.shields.io/badge/Android%20Arsenal-Status%20Bar%20Alert-green.svg?style=flat )]( https://android-arsenal.com/details/1/7037 )

<img src="https://github.com/fede87/StatusBarAlert/raw/master/status_bar_alert_demo.gif" width="330" height="600" />

## What is this?

This is a small library inspired by Telegram X status bar new alert, written in Kotlin.
It shows custom message with optional indeterminate progress in status bar area.
Optional autohide feature can be tweaked with custom duration.
When showing, status bar alert kindly hides status bar's icon with `SYSTEM_UI_FLAG_LOW_PROFILE` flag mode, if avaible from os.

## Supported devices

This lib is supported by every device with a SDK level of at least 14 (Android 4+).


## Quick walkthrough

### Gradle

Add this line to your app's dependecies:

    implementation 'com.fede987:status-bar-alert:1.0.1'

### Quick Sample

Show a new status bar alert :

```
StatusBarAlert.Builder(this@MainActivity)
                       .autoHide(true)
                       .withDuration(100)
                       .showProgress(true)
                       .withText("autohide!")
                       .withAlertColor(R.color.colorPrimaryDark)
                       .build()
```

Hide all status bar alerts for current activity with a `onHidden` callback :

```
StatusBarAlert.hide(this@MainActivity, Runnable {})
```

## License

    Copyright 2018 Federico Marin

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
