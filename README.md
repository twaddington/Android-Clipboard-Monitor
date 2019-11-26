# ClipboardMonitor

This is a sample Android project that monitors the system's ClipboardManager
for changes and logs the clipboard text to a file.

## Update (2019-11-26)

This issue is completely mitigated in Android 10 with this change:

> **Limited access to clipboard data**
>
> Unless your app is the default input method editor (IME) or is the app that currently has focus, your app cannot access clipboard data on Android 10 or higher.

https://developer.android.com/about/versions/10/privacy/changes#clipboard-data

## Security

An electronic clipboard is insecure by nature. Such a system is designed to
facilitate the sharing of data between applications. However, the Android
ClipboardManager is so mind blowingly insecure that any application can
log every piece of data that you copy. This project is designed to illustrate
how trivial this is.

Android developers need to be aware that anything they add to the system
clipboard should be considered public data.

## Recommendations

~~The Android platform should implement a `READ_CLIPBOARD` permission or a
`PasswordEditText` with a supported `PICK_PASSWORD` intent action so users
have more control over what apps have access to the system clipboard.~~

The new [Autofill Framework](https://developer.android.com/guide/topics/text/autofill.html) solves these concerns in Android 8.0.

## License

This code is released under the Apache 2.0 license. See the LICENSE text for
details.
