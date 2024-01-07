---
title: 0x02 - (SK) sknux
layout: page
permalink: 0x02 - (SK) sknux
---

# Script(s) criados por mim com um grau relevante de utilidade:

```javascript
Java.perform(function() {
    var currentActivity;

    // Intercept the call to the 'onCreate' method of all the Activities
    var Activity = Java.use('android.app.Activity');
    Activity.onCreate.overload('android.os.Bundle').implementation = function(savedInstanceState) {

        // Save the reference to the current activity
        this.onCreate.overload('android.os.Bundle').call(this, savedInstanceState);

        currentActivity = this;
        console.log("The current Activity is: " + currentActivity.getClass().getName());

        var stack = Java.use("android.util.Log").getStackTraceString(Java.use("java.lang.Exception").$new())
        console.log("Here is your stacktrace: " + stack);
    }

});
```

## References
[Frida Codeshare - SK](https://codeshare.frida.re/@sknux/stacktracing-activities/)

-------

# Comando(s) úteis do adb (Android Debug Bridge)

```shell
adb shell install-multiples *.apk
adb devices
adb logcat (-c)
```



